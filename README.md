# 有一些不注意就会掉坑里的

###下个月一号
    $today="2019-05-31 10:00:00";
####方式一（正确）
    $opt_time = strtotime(date("Y-m-t", $today)) + 86400; //下个月1号
####方式二（正确）
    $today=date('Y-m', strtotime(today))."-01";//转成每月01去转换就不会有错，因为每月都有1号
    $opt_time=date('Y-m', strtotime("+1 month", strtotime($today))); 

####方式三（错误）
    这个执行出来是有误的，会变成2019-07，因数它会变成 2019-06-31，6月没有31变会变成7月
    $opt_time=date('Y-m', strtotime("+1 month", strtotime($today))); 

###一个月有几天
$days = date("t", $day_time); 
 
 
 

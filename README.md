# 有一些不注意就会掉坑里的

### 下个月一号
    $today="2019-05-31 10:00:00";
#### 方式一（正确）
    //先获取每月最后一天，再+1天的时间戳
    $opt_time = strtotime(date("Y-m-t", $today)) + 86400;
    opt_time=date('Y-m',$opt_time);
    结果：2019-06
#### 方式二（正确）
    //转成每月01，再取下个月1号，（每个月都有一号）
    $today=date('Y-m', strtotime(today))."-01";
    $opt_time=date('Y-m', strtotime("+1 month", strtotime($today))); 
    结果：2019-06
#### 方式三（错误）
    这个执行出来是有误的，会变成2019-07，因数它会变成 2019-06-31，6月没有31变会变成7月
    $opt_time=date('Y-m', strtotime("+1 month", strtotime($today))); 
    结果：2019-07
### 一个月有几天
      $days = date("t", $day_time); 
      
### 前七天
$seven_d=7;
$sevenday = date('Ymd', strtotime('-'.$seven_d.' day')); //前七天 
 

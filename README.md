# 前端面试试题整理
2018年搜索整理
# 1.js如何检测一个变量是string类型：
typeof("asd")  => string
typeof(123)    => number
typeof[]       => object
typeof(qqq)    => undefined
# 2.js如何检测数组
function isArra(obj){
  return typeof(obj) == "object" && obj.constructor == Array
}
# 3.用js去除字符串空格？
# 正则表达式：
str.replace(\/s*/g,"");    => all /s
str.replace(\^/s*/g,"");   => before /s
str.replace(\/s*$/g,"");   =>end  /s
str.replace(\/s*|/s*$/g,"");  => qian hou /s
# jquery trim
$.trim(str);   str.trim();
# 4.获取url中的查询字符参数
function getParam(){
  var shref = window.location.href;
  var args = shref.split("?");
  if(args[0]==shref){
    return " ";
  }else{
    var arrs = args[1].split("&");
    var obj = {};
    for(var i=0; i<arrs.length; i++){
      var arg = arrs[i].split("=");
      obj[arg[0]] = arg[1];
    }
    return obj;
  }
}

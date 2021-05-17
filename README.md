# ChinesePYJs
ChinesePYJs  

## 一.使用js将中文汉字转拼音类库
ChinesePY.js
```
使用方法自己研究
```

## 二.js简单实现汉字转成拼音的功能

最近项目需要一个功能，实现汉字转拼音功能，具体比如说输入一个“你好”，同时带出对应拼音“NiHao”，在此做一下记录

###### 1、首先引入两个文件
```
    <script src="jquery.min.js"></script>
    <script src="Convert_Pinyin.js"></script>
```
###### 2、html设计

```
 <body>
        <div>         
             输入名称：<input type="text" id="chinaName"  onBlur="ConvertName()" />  <br/>  
             全写拼音：<input type="text" id="fullName" /> <br/> 
             简写拼音：<input type="text" id="easyName" /> <br/> 
        </div>    
 </body>
```

###### 3、js方法

```
<script>
       var ConvertName = function(){    
            var chinaName = $('#chinaName').val();    
            //获取全写拼音（调用js中方法）        
            var fullName = pinyin.getFullChars(chinaName);
            //获取简写拼音（调用js中方法）
            var easyName = pinyin.getCamelChars(chinaName);    
            //给两个文本框赋值    
            $('#fullName').val(fullName);
            $('#easyName').val(easyName);
       }
</script>
```

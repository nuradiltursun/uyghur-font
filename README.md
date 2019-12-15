# uyghur-font

通过unicode-range设置字体

### unicode-range

uyghur font unicode-range

```
1. U+0600 to U+06FF
2. U+0750 to U+077F
3. U+FB50 to U+FDFF
4. U+FE70 to U+FEFF

// 代码:
1. U+0600-06FF
2. U+0750-077F
3. U+FB50-FDFF
4. U+FE70-FEFF
```

中文

```
1. U+4E00-9FCB
```

english
```
1. U+00-024F
```

css代码:

```css
 @font-face {
        font-family: "uy-font";
        src: url('./alkatip.TTF');
        unicode-range: 	U+0600-06FF;
    }
  @font-face {
        font-family: 'zh-font';
        src: url('./中文字体');
        unicode-range: U+4E00-9FCB;
    }
  @font-face {
        font-family: 'en-font';
        src: url('./english font');
        unicode-range: U+00-024F;
    }
     *{
      
        font-family: uy-font,zh-font,en-font;
    } 
    

```

就这样自己的首要字体放最前面，一定要最前面，因为有些字体任何unicode都起作用，我们上面的uyfont只能在指定的unicode范围起作用，其他的都用第二个字体，如果维汉英混合使用的话顺序为：维-汉-英；

----
尽量uy-font自己要上传，汉字和英文一般没必要上传，用电脑自带的字体就行，
我一般常用字体如下：

1. uy : 'ALKATIP Asliye'
1. 汉字用：微软雅黑
2. 英文用 ：'Segoe UI'

最终代码:

```
 *{
      
        font-family: uy-font,'微软雅黑','Segoe UI' !important;
       
    }
    @font-face {
        font-family: "uy-font";
        src: url('./alkatip.TTF');
        unicode-range: 	U+0600-06FF;
    }
    
```

最后再重复一点:

```
1. 维吾尔字体要上传,英汉不用，用自带的就行
2. 顺序:维->汉->英
```

Good lucks :)






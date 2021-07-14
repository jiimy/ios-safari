# ios-safari
ios safari 이슈들 모음
```
Safari 6.1+
/* Safari 6.1+ (9.0 is the latest version of Safari at this time) */

@media screen and (min-color-index:0) and(-webkit-min-device-pixel-ratio:0) 
{ @media {
    .safari_only { 

        color:#0000FF; 
        background-color:#CCCCCC; 

    }
}}
Safari 9.0+
/* Safari 9.0+ */

_::-webkit-:not(:root:root), .safari_only {

  color:#0000FF; 
  background-color:#CCCCCC; 

}


Safari 9
/* Safari 9 */

@supports (overflow:-webkit-marquee) and (justify-content:inherit) 
{

  .safari_only {
    color:#0000FF; 
    background-color:#CCCCCC; 
  }

}


아이폰 사파리 9.0이상 만 적용Safari 9.0+ (iOS Only)
/* Safari 9.0+ (iOS Only) */

@supports (-webkit-text-size-adjust:none) and (not (-ms-accelerator:true))
and (not (-moz-appearance:none))
{

  .safari_only {
    color:#0000FF; 
    background-color:#CCCCCC; 
  }

}


사파리 9.0 이상 웹브라우저 만 적용 - Safari 9.0+ (non-iOS)
/* Safari 9.0+ (non-iOS) */

_:-webkit-full-screen:not(:root:root), .safari_only {

  color:#0000FF; 
  background-color:#CCCCCC; 

}


Safari 6.1-7.0
/* Safari 6.1-7.0 */

@media screen and (-webkit-min-device-pixel-ratio:0) and (min-color-index:0)
{  
   .safari_only {(;

      color:#0000FF; 
      background-color:#CCCCCC; 

    );}
}


Safari 7.1+
/* Safari 7.1+ */

_::-webkit-full-page-media, _:future, :root .safari_only {

  color:#0000FF; 
  background-color:#CCCCCC; 

}


사파리 6.1 이상 웹브라우저 만 적용 - Safari 6.1+ (non-iOS)
/* Safari 6.1+ (non-iOS) */

@media screen and (min-color-index:0) and(-webkit-min-device-pixel-ratio:0) 
{ @media {
    _:-webkit-full-screen, .safari_only { 

        color:#0000FF; 
        background-color:#CCCCCC; 

    }
}}
```

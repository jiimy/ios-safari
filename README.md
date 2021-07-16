# ios-safari
ios safari 이슈들 모음

## ios에서만 적용되게 하는 css 
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

## ios 터치꾹 누를시 나오는 설명 제거
https://okjungsoo.wordpress.com/2018/07/24/webkit-touch-callout/
https://developer.mozilla.org/en-US/docs/Web/CSS/-webkit-touch-callout


위 기능이 ios에서만 되기때문에 
@support '기능' 으로 해서 ios판별 가능. 


## pixel ratio 를 이용한 폰 판별
```
// ios 8 대응 pixel-ratio, pixel-ratio ios8 : 2, 노트 10+: 2.5, 아이폰 12pro: 3
@mixin custom-media-ratio($number) {
  @media
  (-webkit-min-device-pixel-ratio: $number)      and (max-width: $breakpoints-mobile+'px'),
  (   min--moz-device-pixel-ratio: $number)      and (max-width: $breakpoints-mobile+'px'),
  (     -o-min-device-pixel-ratio: $number)    and (max-width: $breakpoints-mobile+'px'),
  (        min-device-pixel-ratio: $number)      and (max-width: $breakpoints-mobile+'px')  {

  // @media (max-width: $breakpoints-mobile+'px') and (-webkit-min-device-pixel-ratio: $number),
  // @media (max-width: $breakpoints-mobile+'px') and (min-device-pixel-ratio: $number){
    @content;
  }
}
```

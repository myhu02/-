@@ -20,6 +20,7 @@
-  **康軒** : [國中領域] ( https://webetextbook.knsh.com.tw/2/index.html?code_ Degree=2 )｜[國中輔材] ( https://digitalmaster.knsh.com.tw/ebook/review/ )
-  **翰林** : [翰林行動大師] ( https://edisc3.hle.com.tw/edisc_v3/ebook_v2023.html ) ｜ [翰林雲端命題大師] ( https://testbank.hle.com.tw )｜[翰林輔材網] (
-  **南一**：[ NaniBook 電子書] ( https://reader.oneclass.com.tw/bookshelf )｜[ NaniBox 網頁版] ( https://onebox2.oneclass.com.tw )｜[ NaniPaper 線上雲端出題] ( https://onepaper.twoneclass.com. tw)
-  **奇鼎事業**：[奇鼎數位書櫃] ( https://ebook02.chiding.com.tw/BookCase/publish/index.html )

###書籤版
1 .如果尚未開啟書籤列請以` Ctrl + Shift + B `開啟，然後對書籤列按滑鼠右鍵，選擇「新增網頁...」。
@@ -57,13 +58,13 @@ javascript:(function(){var script=document.createElement('script');script.src='h

![繁體中文] ( https://gist.github.com/assets/121224522/f1e71739-7a86-465b-bae5-965fcef6d23c )

如果你使用的是繁體中文（如上圖），請在控制台輸入「`允許貼上` ”，然後按 Enter 鍵允許貼上。
如果您使用的是繁體中文（如上圖），請在控制台輸入「`允許貼上` ”，然後按 Enter 鍵允許貼上。

![中文] ( https://gist.github.com/assets/121224522/11aa0d00-3684-4b16-b98a-7c0a6deff90b )

如果你使用的是中文（如上圖），請在控制台輸入「`允許貼上`」，並按 Enter 鍵允許貼上。
如果你使用的是中文（如上圖），請在主機控台輸入「`允許貼上`」，並按下Enter鍵允許貼上。

對於其他語言，請在控制台輸入對應中的內容，並按 Enter 鍵允許貼上。
其他語言，請在主控台輸入引號中的內容，並按 Enter 應答鍵允許貼上。
</詳情>

4 .達成交付登錄！
@@ -84,13 +85,13 @@ javascript:(function(){var script=document.createElement('script');script.src='h

![繁體中文] ( https://gist.github.com/assets/121224522/f1e71739-7a86-465b-bae5-965fcef6d23c )

如果你使用的是繁體中文（如上圖），請在控制台輸入「`允許貼上` ”，然後按 Enter 鍵允許貼上。
如果您使用的是繁體中文（如上圖），請在控制台輸入「`允許貼上` ”，然後按 Enter 鍵允許貼上。

![中文] ( https://gist.github.com/assets/121224522/11aa0d00-3684-4b16-b98a-7c0a6deff90b )

如果你使用的是中文（如上圖），請在控制台輸入「`允許貼上`」，並按 Enter 鍵允許貼上。
如果你使用的是中文（如上圖），請在主機控台輸入「`允許貼上`」，並按下Enter鍵允許貼上。

對於其他語言，請在控制台輸入對應中的內容，並按 Enter 鍵允許貼上。
其他語言，請在主控台輸入引號中的內容，並按 Enter 應答鍵允許貼上。
</詳情>

4 .達成交付登錄！
@@ -101,31 +102,51 @@ javascript:(function(){var script=document.createElement('script');script.src='h
**注意事項**：需要先點選要下載的電子書，再切換指令碼才會生效，且每次切換電子書都需要再執行一次。目前僅支援國中的電子書，國小電子書和媒體盒可暫時改用evonisme製作的[ EvGo ] ( https://github.com/evonisme/EvGo/tree/main )下載。造成不便，稍後見執行。
``` js
if ( window.location.href.startsWith ( “ https://webetextbook.knsh.com.tw/ ” ) ) {
  var執行=  false ;
  document.querySelectorAll ( ' .downAssetBtn ' ) .forEach ( function ( button ) {
    if ( ! executed && ( ! document.getElementById ( ' assetsPage ' ) || document.getElementById ( ' assetsPage ' ) . style.display === ' none ' ) ) {   
      alert ( '請先點選您要使用的電子書，再執行指令碼。' );
      已執行= 真；
    } else  if（！執行）{
      var link =  document.createElement ( ' a ' ) ;
      if ( window.location.href.startsWith ( “ https://webetextbook.knsh.com.tw/webcase/index.html ” ) ) {
        連結. href  =  ' https://storage1.knsh.com.tw/material/ '  + 按鈕. getAttribute ( ' d-file_name ' );
        關聯。textContent  =  '下載' ;
      } else  if ( window.location.href.startsWith ( “ https://webetextbook.knsh.com.tw/2/index.html ” ) ) { https://webetextbook.knsh.com.tw/2/index.html ” ) ) {
        link.href = ' https://webetextbook.knsh.com.tw/Ebookvieweran4Teacher/index.html?id= ' +（button.getAttribute ( ' d - file_name '  ) ? button.getAttribute ( ' d - file_name ' ) .replace ( ' button.getAttribute ( ' d - file_name ' ) .replace ( ' .    
        關聯。textContent  =  '開啟' ;
  const  assetButtons  =  document.querySelectorAll ( ' .downAssetBtn ' ) ;
  讓hasFileName =  false ;
  assetButtons.forEach (按鈕= > { 
    const  fileName  = 按鈕.getAttribute ( ' d - file_name ' );
    如果（檔名）{
      hasFileName =  true ;
      const  label  =  document.createElement ( ' a ' ) ;
      標籤. href  =  ` https://webetextbook.knsh.com.tw/Ebookvieweran4Teacher/index.html?id=${fileName . replace ( ' .zip ' , ' ' ) } ` ;
      標籤。textContent  =  '開啟' ;
      標籤.className = ' m- 0 標籤標籤資訊' ; 
      按鈕.innerHTML = ' ' ;    
      按鈕.appendChild (標籤) ;
      按鈕.removeAttribute ( ' onclick ' ) ;
    }
  });
  如果（hasFileName）{
    安慰。log ( '執行成功！' );
  }別的{
    alert ( '請先點選您要使用的電子書，再執行指令碼。' );
  }
} else  if ( window . location . href . startsWith ( ' https://digitalmaster.knsh.com.tw/v3/pages/j/index.html ' )) {
  讓alertShown =  false ;
  document.querySelectorAll ( ' . downloadButton ' ) . forEach ( button => { 
    const  urlMatch  =  button.getAttribute ( ' onclick ' ) ?. match ( / openeRefbook \( '( . * ? )' \ ) / ) ;
    如果（urlMatch ？ .[ 1 ]）{
      const  curBookUrl  =  new  URL (urlMatch[ 1 ]) . searchParams.get ( ' CUR_BOOK_URL ' ) ;
      如果（curBookUrl）{
        如果（！ alertShown）{
          警報（` CUR_BOOK_URL：${ curBookUrl } `）；
          alertShown =  true ;
          按鈕。textContent  =  "免登錄開啟" ;
          按鈕.removeAttribute ( ' onclick ' ) ;
          按鈕. addEventListener ( '點擊' , () => 視窗. open (urlMatch[ 1 ], ' _blank ' ));
        }
        返回;
      }
      按鈕.innerHTML = ' ' ;  
      按鈕.appendChild (連結)；
      本地儲存。setItem ( "登入帳號" , "模擬帳號" ); //設定假帳號
      本地儲存。setItem ( “ uuid ” , “ mockUUID ” ); //設定假UUID
}})} else  if ( window . location . href . startsWith ( ' https://digitalmaster.knsh.com.tw/downloader/box-web/index.html ' )) {
    }
  });
} else  if ( window . location . href . startsWith ( ' https://digitalmaster.knsh.com.tw/downloader/box-web/index.html ' )) {
  alert ( '請先選擇要使用的年級再執行指令碼。' );
} else  if ( window . location . href . startsWith ( ' https://digitalmaster.knsh.com.tw/ebook/review/ ' )) {
  alert ( '請先選擇要使用的電子書再執行指令碼。' );
} else  if ( confirm ( '網站錯誤，請選擇要開啟的項目：\n\n 1.國中領域\n 2.國中輔材' )) {
  var selectedURL = [ ' https://webetextbook.knsh.com.tw/2/index.html?code_ Degree=2 ' , ' https://digitalmaster.knsh.com.tw/ebook/review/ ' ][ parseInt ( prompt ( '請輸入你的選擇（輸入數字 1 或 2 )：1  ] ;
  selectedURL &&  window.open ( selectedURL , ' _blank ' ) ;
  const  selectedURL  = [ ' https://webetextbook.knsh.com.tw/2/index.html?code_ Degree=2 ' , ' https://digitalmaster.knsh.com.tw/ebook/review/ ' ][ parseInt ( Prompt ( '請輸入你的選擇（輸入數字 1 或 2 )：1  ] ;
  如果（selectedURL） 視窗.開啟（selectedURL，' _blank '）；
}
` ` `
@@ -151,7 +172,7 @@ if (window.location.href.startsWith("https://edisc3.hle.com.tw/edisc_v3")) {
if ( window.location.href.includes ( “ oneclass.com.tw ” ) ) {
  讓mockToken =  JSON.stringify ( {
  “代碼”： “成功”，
  jwt ：eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJpc3MiOiJodHRwOi8vbXlhY2NvdW50Lm5hbmkuY29vbC8iLCJzd WIiOiJ1c2Vycy91bmljeWNsZTQiLCJmcm9tIjoiTmFuaSIsInVzZXJuYW1lIjoidW5pY3ljbGU0IiwiZW1haWx2YWxp ZCI6dHJ1ZSwibW9iaWxldmFsaWQiOmZhbHNlLCJlbWFpbCI6ImtyNTJ5NTRtQGR1Y2suY29tIiwidWlkIjoiND​ A3YzBhNjAtMzgxZS0xMWVmLWEyZjMtMGYxNmE0Y2MyYjA4IiwianRpIjoiY2FjNDAzYjAtZjkyYS00YmY1LTg0MDktN WM1OTk1OGEwMTIxIiwiaWF0IjoxNzE5ODg4ODQzLCJleHAiOjE3MjUwNzI4NDN9.-usPxm8q72YvcAkqqdRSYoxVC-h2K862EV8DCtMZQCI “ ); 
  jwt ：eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJpc3MiOiJodHRwOi8vbXlhY2NvdW50Lm5hbmkuY29vbC8iLCJzd WIiOiJ1c2Vycy91bmljeWNsZTQiLCJmcm9tIjoiTmFuaSIsInVzZXJuYW1lIjoidW5pY3ljbGU0IiwiZW1haWx2YWxp ZCI6dHJ1ZSwibW9iaWxldmFsaWQiOmZhbHNlLCJlbWFpbCI6ImtyNTJ5NTRtQGR1Y2suY29tIiwidWlkIjoiND​ A3YzBhNjAtMzgxZS0xMWVmLWEyZjMtMGYxNmE0Y2MyYjA4IiwianRpIjoiMzEzNGE2ZDAtZTc0Zi00MDM0LTkzNjItM DY2YmI0NzA0YTcwIiwiaWF0IjoxNzI1MDczMzUyLCJleHAiOjE3MzAyNTczNTJ9.UIiK2nzCpv-F-LKYBWDEgsQQ5AdyW92tH5U9_t9Couo “ }); 
  讓欄位名稱=  " nani_oneclass_login_token " ;
  var d =  new  Date ();
  d . setTime ( d.getTime () + ( 1 * 24 *  60 * 60 * 1000  ) ) ;      
@@ -176,7 +197,7 @@ if (window.location.href.includes("oneclass.com.tw")) {
if ( window.location.href.startsWith ( “ https://testbank.hle.com.tw ” ) ) {
  localStorage.setItem("oidc.user:https://id.hle.com.tw:js", '{“access_token”：“eyJhbGciOiJSUzI1NiIsImtpZCI6Ijg1NzgwNWYxZGQ3ZmE5YTZiNTI3ZjQ0ZWNmZmJkNDhjIiwidHlwIjoiYXQQCInll-mZmJkJIiiwidHlwIjoiYXQQTInll CI6dHJ1ZSwibG9jayI6ZmFsc2UsInZlciI6Mywic2NvcGUIOlsib3BlbmlkIiwicHJvZm lsZSJdLCJhbXIiOlsicHdkIl19.d5gF0rVVmO_u28ZVVmO1 dQ0jjrqbyD0V0zlDpmDmnSBgJFoFVztO05cgQcwVzTwrFETG6c2t5zUESIUM0tEvvIlFNhGU1IQV6VNYxZJylghHCvwgONTBpjQUzbIxFnYIb4LNYxZJylghHCvwgONTBpjQUzbIxFnYIb4L144L1 uCwm2fF2gCao9Y9wl-BvruDtE5Oh0hyr7G8cBb0MefbBkd4aAwCUbxi1T-XQzTI​​XUPFl9TJq7ZQ6Rs-4gmj0edlsEv17sGFMFl9TJq7ZQ6Rs-4gmj0edlsEv17sGFMFl9TJq7ZQ6Rs-4gmj0edls wAixpYS7dwTKxRFDFXMxA","id_token":"eyJhbGciOiJSUzI1NiIsImtpZCI6Ijg1NzgwNWYxZGQ3ZmE5YTZiNTI3ZjQ0ZWNmZmJkNDhjIiwIHM​​ilwM​​iHlkNDhjIiw. WRlbnRpZmllZCI6dHJ1ZSwibG9jayI6ZmFsc2UsInZlciI6MywiYW1yIjpbInB3ZCJdfQ .v2vYQXQGgBDKgY6ggyy4V1Xv_K7aEz2vYQXGgBDKgY6g YCiD8qlNRb_D2Qp4AwC3q0L7j6l-qtEyrpzF7qI4LaWNw6N_MRKaP5m9-Zc9c6q1Q1miX yjFvjBJcwc3f2VdXEa5d49Qg9yHhdi3Y6RbQim8fuz-HR7MexEc94RGf0FS5Rc2EbixlEt kiYtziM9LfIRXskfy-wkUWdrHwwC7A_qQnuMiKIyUfQr0MEP9lH-lMZv6XtB0EapmfP4E wgTIK4Ak_dvzWQEffhyT36QbkmDkHYbQk1if9BcriXXgJgZ0Pz433_ETDgEHlULJg”}');
  地點。重新載入（）；//重新載入網頁
} else  if ( window .confirm ( "網站錯誤，按「確定」來開啟網站。" )) {
} else  if ( window .confirm ( "網站錯誤，按一下「確定」來開啟翰林雲端命題大師。" )) {
  window.open ( ' https : //testbank.hle.com.tw','_blank ' ) ;
}
` ` `
@@ -194,42 +215,42 @@ if (window.location.href.startsWith("https://reference.hle.com.tw")) {
` ` `
### ✅奇鼎事業
連結：[奇鼎事業] ( https://ebook02.chiding.com.tw/BookCase/publish/index.html )
連結：[奇鼎數位書櫃](https://ebook02.chiding.com.tw/BookCase/publish/index.html)
` ` ` js
if ( window.location.href.startsWith ( “ https://ebook02.chiding.com.tw/BookCase/publish/index.html ” ) ) {
    var執行=  false ;
    document.querySelectorAll ( ' .downAssetBtn ' ) .forEach ( function ( button ) {
      if ( ! executed && ( ! document.getElementById ( ' assetsPage ' ) || document.getElementById ( ' assetsPage ' ) . style.display === ' none ' ) ) {   
        alert ( '請先點選您要使用的電子書，再執行指令碼。' );
        已執行= 真；
      } else  if（！執行）{
        var link =  document.createElement ( ' a ' ) ;
          link.href = ' https://ebook02.chiding.com.tw/EbookViewer/publish/Ebook.html?id= ' + ( button.getAttribute ( ' d - file_name ' ) ? button.getAttribute ( ' d -  file_name ' ) .replace ( ' . ) ' , ' ) : '​​​    
          關聯。textContent  =  '開啟' ;
        按鈕.innerHTML = ' ' ;  
        按鈕.appendChild (連結)；
        本地儲存。setItem ( "登入帳號" , "模擬帳號" ); //設定假帳號
        本地儲存。setItem ( “ uuid ” , “ mockUUID ” ); //設定假UUID
  }})}
const  processedButtons  =  new  Set ();
函數 更新按鈕（）{
  if ( ! window.location.href.startsWith ( " https://ebook02.chiding.com.tw/ " ) ) {
    if ( window .confirm ( "網站錯誤，按「確定」來開啟奇鼎數位書櫃。" ) ) {
      window.open ( ' https://ebook02.chiding.com.tw/BookCase/publish/index.html','_blank ' ) ;
    }
    返回;
  }
  document.querySelectorAll ( ' .downAssetBtn ' ) .forEach (按鈕= > { 
    const  fileName  = 按鈕.getAttribute ( ' d - file_name ' );
    如果（檔案名稱&&  ！processedButtons。有（按鈕））{
      按鈕。內部 HTML  =  ' ' ; //清空按鈕內容
      按鈕。移除屬性( ' onclick ' ); //刪除舊的onclick事件
      const  label  =  document.createElement ( '標籤' ) ;
      標籤。textContent  =  '免登錄開啟' ;
      標籤.className = ' m- 0 標籤標籤資訊' ; 
      標籤.樣式.字體大小 =  '16 .5px ' ;
      label.onclick = ( ) = > window.open ( ` https://ebook02.chiding.com.tw/EbookViewer/publish/Ebook.html?id=$ { fileName.replace ( ' .zip ' , ' ' ) } ` , ' _ blank ' ) ;  
      按鈕。附加子（標籤）；//新增標籤
      處理過的按鈕。新增（按鈕）；//標記為已處理
      安慰。log ( `標籤已新增：${ fileName } ` );
    }
  });
}
新的 MutationObserver (updateButtons) .observe ( document.body，{childList : true  ， subtree :  true } );
更新按鈕(); //立即執行
` ` `
>最後測試時間：2024/9/22
>最後測試時間：2024/9/29
</詳情>
### ❌ 目前無效
<詳細資料>
    <summary>按這裡展開</summary>
### ❌康軒總複習即測卷
連結：[康軒總複習即測卷] ( https://ttrplatform.knsh.com.tw/teacher )
``` js
if ( window.location.href.startsWith ( “ https://ttrplatform.knsh.com.tw/ ” ) ) {
  文件. cookie = “ connect.sid=s%3AXM5bGeC2DRBIbxOybL3jxaUHrWUhone4.L298aSJXZtxyUyXBV6UTk4I5rYoWAJ0OYi1VyTfl% 2BXs ”  ； 
  視窗.位置.href = “ https://ttrplatform.knsh.com.tw/teacher ” ;  
} else  if ( window .confirm ( "網站錯誤，按一下「確定」來開啟翰林行動大師。" )) {
  window.open ( ' https://ttrplatform.knsh.com.tw/teacher','_blank ' ) ;
}
```

### ❌何嘉仁電子書
連結：[何嘉仁電子書櫃](https://bookonline.hess.com.tw/bookcase/#/)
` ` ` js
@notlin4 notlin4 修改了 這個要點2024年9月23日。
 修改了 1 個文件 ，其中 新增 1 項 ， 刪除 1 項。
 2 處修改：1 處新增 & 1 處刪除2 
without-auth_e-book_tutorial_免登錄電子書教學.md
原始文件行號	不同行號	差異線變化
@@ -296,7 +296,7 @@ if (!localStorage.getItem("isLogin")) {
-感謝** <ins> @foxvegajian </ins> **提供康軒網頁媒體盒的下載方法。 ( [原訊息] ( https://gist.github.com/aliyaliu368/891eef75e09494e965d291ead4a80d17?permalink_comment_id=4685986#gistcomment-4685986 ) ）
-感謝** <ins> @ J56tw </ins> **提供康軒電子書的免登入方法。( [原訊息] ( https://gist.github.com/notlin4/a05d7db77cd5606a812f4b9900fef3ee?permalink_comment_id=4788981#gistcomment-4788981 )）
-感謝** < ins > @ tmyrhs3 </ ins > **提供翰林帳號。 （[原訊息] ( https://gist.github.com/notlin4/a05d7db77cd5606a812f4b9900fef3ee?permalink_comment_id=4814684#gistcomment-4814684 )）
- 趕寫 ** <ins> @小哲<ins>提供奇鼎事業的免登入方法（Discord ）
- 感謝 ** <ins> @小哲<ins> **提供奇鼎事業的免登錄方法（Discord ）
-最後感謝所有回答別人問題的人！

如果你覺得這篇教學對你有幫助，請點選本篇教學最上方的星星圖標，支持我繼續製作下去！
@notlin4 notlin4 修改了 這個要點2024年9月22日。
 修改了 1 個文件 ，其中 新增 1 項 ， 刪除 5 項。
 6 處修改：1 處添加，5 處刪除6 
without-auth_e-book_tutorial_免登錄電子書教學.md
原始文件行號	不同行號	差異線變化
@@ -18,9 +18,8 @@

###支援網站
-  **康軒** : [國中領域] ( https://webetextbook.knsh.com.tw/2/index.html?code_ Degree=2 )｜[國中輔材] ( https://digitalmaster.knsh.com.tw/ebook/review/ )
-  **翰林** : [翰林行動大師] ( https://edisc3.hle.com.tw/edisc_v3/ebook_v2023.html )｜[翰林雲端命題大師] ( https://testbank.hle.com.tw )｜[翰林輔材網] ( https: //reference.hle.com.twence )｜[翰林輔材網] (h.com https://www.hle.com.tw/ )
-  **翰林** : [翰林行動大師] ( https://edisc3.hle.com.tw/edisc_v3/ebook_v2023.html ) ｜ [翰林雲端命題大師] ( https://testbank.hle.com.tw )｜[翰林輔材網] (
-  **南一**：[ NaniBook 電子書] ( https://reader.oneclass.com.tw/bookshelf )｜[ NaniBox 網頁版] ( https://onebox2.oneclass.com.tw )｜[ NaniPaper 線上雲端出題] ( https://onepaper.twoneclass.com. tw)
-  **何嘉仁**：[何嘉仁電子書櫃] ( https://bookonline.hess.com.tw/bookcase/#/ )

###書籤版
1 .如果尚未開啟書籤列請以` Ctrl + Shift + B `開啟，然後對書籤列按滑鼠右鍵，選擇「新增網頁...」。
@@ -107,9 +106,6 @@ if (window.location.href.startsWith("https://webetextbook.knsh.com.tw/")) {
    if ( ! executed && ( ! document.getElementById ( ' assetsPage ' ) || document.getElementById ( ' assetsPage ' ) . style.display === ' none ' ) ) {   
      alert ( '請先點選您要使用的電子書，再執行指令碼。' );
      已執行= 真；
    } else  if ( ! executed &&  button .getAttribute ( ' d - title ' ) .includes ( " (網頁版) " )) {
      alert ( '偵測到國小電子書，目前不支持繞過國小電子書，請暫時改用evonisme製作的EvGo下載。造成不便之處，我們見諒。' );
      已執行= 真；
    } else  if（！執行）{
      var link =  document.createElement ( ' a ' ) ;
      if ( window.location.href.startsWith ( “ https://webetextbook.knsh.com.tw/webcase/index.html ” ) ) {
@notlin4 notlin4 修改了 這個要點2024年9月22日。
 修改了 1 個文件 ，新增 62 項 ， 刪除 47 項。
 109 處修改：62 處添加，47 處刪除109 
without-auth_e-book_tutorial_免登錄電子書教學.md
原始文件行號	不同行號	差異線變化
@@ -16,8 +16,8 @@
以下指令碼託管於儲存庫[ without -auth_e-book/fast.js ] ( https://github.com/notlin4/without-auth_e-book/blob/main/fast.js )，並使用[ jsDelivr ] ( https://www.jsdelivr.com/ )快取資料，更新日誌可在[這裡] (jsdelivr.com/ )快取資料，更新日誌可在[這裡] https://github.com/notlin4/without-auth_e-book/commits/main/fast.js ）查看。  
**請勿更改以下所有帳號的個人資料！**

###支援網站：
-  **康軒** : [國小領域] ( https://webetextbook.knsh.com.tw/2/index.html?code_ Degree=1 ) ｜[國小英語] ( https://webetextbook.knsh.com.tw/2/index.html?code_ Degree=3 ) ｜[國中領域https://webetextbook.knsh.com.tw/2/index.html?code_ Degree= 2 )｜[國中輔材] ( https://digitalmaster.knsh.com.tw/ebook/review/ ) ｜[網頁媒體盒] ( https://digitalmaster.kdownsh.com./web.kdownshbox .
###支援網站
-  **康軒** : [國中領域] ( https://webetextbook.knsh.com.tw/2/index.html?code_ Degree=2 )｜[國中輔材] ( https://digitalmaster.knsh.com.tw/ebook/review/ )
-  **翰林** : [翰林行動大師] ( https://edisc3.hle.com.tw/edisc_v3/ebook_v2023.html )｜[翰林雲端命題大師] ( https://testbank.hle.com.tw )｜[翰林輔材網] ( https: //reference.hle.com.twence )｜[翰林輔材網] (h.com https://www.hle.com.tw/ )
-  **南一**：[ NaniBook 電子書] ( https://reader.oneclass.com.tw/bookshelf )｜[ NaniBox 網頁版] ( https://onebox2.oneclass.com.tw )｜[ NaniPaper 線上雲端出題] ( https://onepaper.twoneclass.com. tw)
-  **何嘉仁**：[何嘉仁電子書櫃] ( https://bookonline.hess.com.tw/bookcase/#/ )
@@ -96,9 +96,10 @@ javascript:(function(){var script=document.createElement('script');script.src='h

4 .達成交付登錄！

### ✅ 康軒電子書與網頁媒體盒
連結：[國小領域] ( https://webetextbook.knsh.com.tw/2/index.html?code_ Degree=1 )｜[國小英文] ( https://webetextbook.knsh.com.tw/2/index.html?code_ Degree =3 )｜[國中領域＜)｜[國中輔材] ( https://digitalmaster.knsh.com.tw/ebook/review/ )｜[網頁媒體盒] ( https://digitalmaster.knsh.com.tw/downloader/box-web/index.html )  
**注意事項**：需要先點選要下載的電子書，再執行指令碼才會生效，且每次切換電子書都需要再執行一次。目前電子書尚未支援一到五年級的內容，可改用網頁媒體盒進行下載。造成不便之處，小見諒解。

### ✅ 康軒電子書
連結：[國中領域] ( https://webetextbook.knsh.com.tw/2/index.html?code_ Degree=2 )｜[國中輔材] ( https://digitalmaster.knsh.com.tw/ebook/review/ )  
**注意事項**：需要先點選要下載的電子書，再切換指令碼才會生效，且每次切換電子書都需要再執行一次。目前僅支援國中的電子書，國小電子書和媒體盒可暫時改用evonisme製作的[ EvGo ] ( https://github.com/evonisme/EvGo/tree/main )下載。造成不便，稍後見執行。
``` js
if ( window.location.href.startsWith ( “ https://webetextbook.knsh.com.tw/ ” ) ) {
  var執行=  false ;
@@ -107,15 +108,15 @@ if (window.location.href.startsWith("https://webetextbook.knsh.com.tw/")) {
      alert ( '請先點選您要使用的電子書，再執行指令碼。' );
      已執行= 真；
    } else  if ( ! executed &&  button .getAttribute ( ' d - title ' ) .includes ( " (網頁版) " )) {
      alert ( '偵測到一到五年級的內容，目前不支持繞過一到五年級的電子書，請改用網頁媒體盒進行下載。造成不便之處，我們見諒。' );
      alert ( '偵測到國小電子書，目前不支持繞過國小電子書，請暫時改用evonisme製作的EvGo下載。造成不便之處，我們見諒。' );
      已執行= 真；
    } else  if（！執行）{
      var link =  document.createElement ( ' a ' ) ;
      if ( window.location.href.startsWith ( “ https://webetextbook.knsh.com.tw/webcase/index.html ” ) ) {
        連結. href  =  ' https://storage1.knsh.com.tw/material/ '  + 按鈕. getAttribute ( ' d-file_name ' );
        關聯。textContent  =  '下載' ;
      } else  if ( window.location.href.startsWith ( “ https://webetextbook.knsh.com.tw/2/index.html ” ) ) { https://webetextbook.knsh.com.tw/2/index.html ” ) ) {
        link . href  =  ' https://webetextbook.knsh.com.tw/  Ebookviewer4Teacher / Ebook .html ?id = ' +（ button . getAttribute ( ' d - file_name ' ) ?  button . getAttribute ( ' d - file_name ' ) . replace ( ' . 
        link . href  =  ' https://webetextbook.knsh.com.tw/ Ebookvieweran4Teacher/index  .html ?id= ' +（ button . getAttribute ( ' d -file_name ' ) ? button  .getAttribute ( ' d -file_name ' ) . replace ( ' button ' , ' .ipz ) ; 
        關聯。textContent  =  '開啟' ;
      }
      按鈕.innerHTML = ' ' ;  
@@ -126,23 +127,12 @@ if (window.location.href.startsWith("https://webetextbook.knsh.com.tw/")) {
  alert ( '請先選擇要使用的年級再執行指令碼。' );
} else  if ( window . location . href . startsWith ( ' https://digitalmaster.knsh.com.tw/ebook/review/ ' )) {
  alert ( '請先選擇要使用的電子書再執行指令碼。' );
} else  if ( confirm ( '網站錯誤，請選擇要開啟的項目：\n\n 1.國小領域\n 2.國小英語\n 3.國中領域\n 4.國中輔材\n 5.網頁媒體盒' )) {
  var selectedURL = [ ' https://webetextbook.knsh.com.tw/2/index.html?code_ Degree= 1 ' , ' https://webetextbook.knsh.com.tw/2/index.html?code_ Degree = 3 ' , ' https://webetextbook.tw/2/index.html?code_ Degree = 3 ' , ' https://webetextbook.M. digitalmaster.knsh.com.tw/ebook/review/ ' , ' https://digitalmaster.knsh.com.tw/downloader/box-web/index.html ' ][ parseInt ( prompt ( '請輸入你的選擇（輸入數字 1 、2、3、4或5 )：' ) - 11 ]; 
} else  if ( confirm ( '網站錯誤，請選擇要開啟的項目：\n\n 1.國中領域\n 2.國中輔材' )) {
  var selectedURL = [ ' https://webetextbook.knsh.com.tw/2/index.html?code_ Degree= 2 ' , ' https://digitalmaster.knsh.com.tw/ebook/review/ ' ] [ parseInt ( Prompt ( '請輸入你的選擇（輸入數字' 
  selectedURL &&  window.open ( selectedURL , ' _blank ' ) ;
}
```

### ✅康軒總複習即測卷
連結：[康軒總複習即測卷] ( https://ttrplatform.knsh.com.tw/teacher )
``` js
if ( window.location.href.startsWith ( “ https://ttrplatform.knsh.com.tw/ ” ) ) {
  文件. cookie = “ connect.sid=s%3AXM5bGeC2DRBIbxOybL3jxaUHrWUhone4.L298aSJXZtxyUyXBV6UTk4I5rYoWAJ0OYi1VyTfl% 2BXs ”  ； 
  視窗.位置.href = “ https://ttrplatform.knsh.com.tw/teacher ” ;  
} else  if ( window .confirm ( "網站錯誤，按一下「確定」來開啟翰林行動大師。" )) {
  window.open ( ' https://ttrplatform.knsh.com.tw/teacher','_blank ' ) ;
}
```

### ✅ 翰林電子書
連結：[翰林行動大師] ( https://edisc3.hle.com.tw/edisc_v3/ebook_v2023.html )  
``` js
@@ -151,7 +141,8 @@ if (window.location.href.startsWith("https://edisc3.hle.com.tw/edisc_v3")) {
  本地儲存。setItem ( “ last_signinX_v2023 ” ,時間); //將帳號登錄日期設定為目前時間，避免被取代為過渡
  本地儲存。setItem ( " roleX_v2023 " , "老師" ); //將身分設為老師
  本地儲存。setItem ( " emailX_v2023 " , " test@test.com " ); //由於翰林電子書會驗證是否有設定郵件，只要設定即可使用
  localStorage.setItem("tokenX_v2023", “eyJhbGciOiJSUzI1NiIsImtpZCI6Ijg1NzgwNWYxZGQ3ZmE5YTZiNTI3ZjQ0ZWNmZmJkNDhjjIiwidlw. 7YvKu2zsD4t8JoYLtUHeKopyBAb-mxneB3hU0Ejdt_-9iI-4z60_KEAnzLeBp2Gv0SSxpBgFdweRn31MIP4WHGCfpq4rPAGmdIpnWPUBTYywRcpnWPUB F7JOV_23qZIsyfXcj78K_FnBJwGuaT6J4oiyNSmuWjV7mx8tMj0IHINK3C5IJKmDDOX9ymmCk5WQ2mLuckjgel3uWoFxZTwT1mOxrVqGHmgYVo hrrt8f3YJuzLfoHxCmVQ6AW8zdc9OKi4xtaYwhHxjEOHZ5GFZ45uorWRxLIcuukdLLpUgQMl7awnL6yXbT-En7Bxzw-5v8P0WFhSI4tS8bHgSI4tS8bHg”；
  本地儲存。setItem ( “ lockX_v2023 ” , “假” );
  localStorage.setItem("tokenX_v2023", “eyJhbGciOiJSUzI1NiIsImtpZCI6Ijg1NzgwNWYxZGQ3ZmE5YTZiNTI3ZjQ0ZWNmZmJkNDhjIiwidH lwIjoiYXQrand0In0.-WwjyIsImlzaWRlbnRpZmllZCI6dHJ1ZSwibG9jayI6ZmFsc2UsInZlciI6Myw ic2NvcGUiOlsib3BlbmlkIiwicHJvZmlsZSIsImFwaTEiLCJJZGVudGl0eVNlcnZlckFwaSIsImhhbmx pbi1hcGkiLCJvZmZsaW5lX2FjY2VzcyJdLCJhbXIiOlsicHdkIl19.PGXhy1RBo_ff1lzvinDS8pR7qO eeotbQTaaW8kRRaF35Ga9QnhFM1FArfHXofPwNQvwok7KLfOosCA8iegJC2dN2EZPSflZMHD8VPn4UZ 6ZJTSAXt2s_T-hm6MEZM9iNoDerlam9G64evmtfrW0qygnLrMqVjGxVxXiy0pOM-8VcVMkc-iBNzZRV- vxnokS0jqQCTwAdkVMKCuFksrpRNtg2HLAAwVPosey5rjnBH4ivIMUey1dbZzaHRQwdZ3_ZDM5h9-j_1 LKGvrVpNQ-VcLc2-iShUVbb0bxwCzpkmTJ1ySSH4edZV36rFgXQNcDASARC5ujBUVQ79Brc6hR37w"); // 設定驗證用的權限
  地點。重新載入（）；//重新載入網頁
} else  if ( window .confirm ( "網站錯誤，按一下「確定」來開啟翰林行動大師。" )) {
  window.open ( ' https://edisc3.hle.com.tw/edisc_v3/ebook_v2023.html','_blank ' ) ;
@@ -183,24 +174,11 @@ if (window.location.href.includes("oneclass.com.tw")) {
}
```

### ✅ 何嘉仁電子書
連結：[何嘉仁電子書櫃] ( https://bookonline.hess.com.tw/bookcase/#/ )
``` js
if ( window.location.href.startsWith ( “ https://bookonline.hess.com.tw/bookcase/#/ ” ) ) {
if ( ! localStorage.getItem ( " isLogin " ) ) {
  本地儲存。setItem ( “ isLogin ” , “ true ” ); //將登入狀態設為true
  本地儲存。setItem ( " uuid " , " mock_user " ); //設定假的教師UUID
  地點。重新載入（）；//重新載入網頁
}} else  if ( window .confirm ( "網站錯誤，按一下「確定」來開啟何嘉仁電子書。" )) {
  window.open ( ' https://bookonline.hess.com.tw/bookcase/#/','_blank ' ) ;
}
```

### ✅ 翰林雲端命題大師
連結：[翰林雲端命題大師] ( https://testbank.hle.com.tw )
``` js
if ( window.location.href.startsWith ( “ https://testbank.hle.com.tw ” ) ) {
  localStorage.setItem("oidc.user:https://id.hle.com.tw:js", '{“access_token”：“eyJhbGciOiJSUzI1NiIsImtpZCI6Ijg1NzgwNWYxZGQ3ZmE5YTZiNTI3ZjQ0ZWNmZmJkNDhjIiwidHlwIjoiYXQrand0In0iYXQrand0In0 ..tRzJFMcjaxDj7YvKu2zsD4t8JoYLtUHeKopyBAb-mxneB3hU0Ejdt_-9iI-4z60_KEAnzLeBp2Gv0SSxpBgFdweRn31MIP4WHGCfpqLeBp2Gv0SSxpBgFdweRn31MIP4WHGCfpq4rPAGImd WPUBTYywRcXF7JOV_23qZIsyfXcj78K_FnBJwGuaT6J4oiyNSmuWjV7mx8tMj0IHINK3C5IJKmDDOX9ymmCk5WQ2mLuckjglel3uWoFxZTwT1mOx qGHmgYVohrrt8f3YJuzLfoHxCmVQ6AW8zdc9OKi4xtaYwhHxjEOHZ5GFZ45uorWRxLIcuukdLLpUgQMl7awnL6yXbT-En7Bxzw-5v8P0WFhSI4tS8b Hg","id_token":"eyJhbGciOiJSUzI1NiIsImtpZCI6Ijg1NzgwNWYxZGQ3ZmE5YTZiNTI3ZjQ0ZWNmZmJkNDhjIiwidHlwIjoiNTI3ZjQ0ZWNmZmJkNDhjIiwidHlwIjoiSldUIn0..cySod WB702wd4_IXGXWuwcas0m7jUL2VSCUnmHcTWKpNy7GPZTJv5FjMHVISwpViS8pxrWnKzd0YA3xCAopo7XB0_n1W8OjPb82dALd4nt-9xCAopo7XB0_n1W8OjPb82dALd4nt-9ozP0IedAOEo ji_2XoTf-TtBSCtsOFa6H6WZtRG4In8v-8fVLYrBVTdVs9mSiGAn_W7GQiI-fhbb6G3MM3ctKoPLg-0LmVELDbp0gFKNUbIQhpxIKS3M3ctIkpl3-f 2mT9OiGlgFieY6xhNpSyPCqnFA7HSvMHfJFYlgOfU2RdEJyZQSitbLYEsh-vNZrufrewpxW6Bdc4AqI4U_KXOrOoo1T7TowBWOg7dxLPHhw}'');
  localStorage.setItem("oidc.user:https://id.hle.com.tw:js", '{“access_token”：“eyJhbGciOiJSUzI1NiIsImtpZCI6Ijg1NzgwNWYxZGQ3ZmE5YTZiNTI3ZjQ0ZWNmZmJkNDhjIiwidHlwIjoiYXQQCInll-mZmJkJIiiwidHlwIjoiYXQQTInll CI6dHJ1ZSwibG9jayI6ZmFsc2UsInZlciI6Mywic2NvcGUIOlsib3BlbmlkIiwicHJvZm lsZSJdLCJhbXIiOlsicHdkIl19.d5gF0rVVmO_u28ZVVmO1 dQ0jjrqbyD0V0zlDpmDmnSBgJFoFVztO05cgQcwVzTwrFETG6c2t5zUESIUM0tEvvIlFNhGU1IQV6VNYxZJylghHCvwgONTBpjQUzbIxFnYIb4LNYxZJylghHCvwgONTBpjQUzbIxFnYIb4L144L1 uCwm2fF2gCao9Y9wl-BvruDtE5Oh0hyr7G8cBb0MefbBkd4aAwCUbxi1T-XQzTI​​XUPFl9TJq7ZQ6Rs-4gmj0edlsEv17sGFMFl9TJq7ZQ6Rs-4gmj0edlsEv17sGFMFl9TJq7ZQ6Rs-4gmj0edls wAixpYS7dwTKxRFDFXMxA","id_token":"eyJhbGciOiJSUzI1NiIsImtpZCI6Ijg1NzgwNWYxZGQ3ZmE5YTZiNTI3ZjQ0ZWNmZmJkNDhjIiwIHM​​ilwM​​iHlkNDhjIiw. WRlbnRpZmllZCI6dHJ1ZSwibG9jayI6ZmFsc2UsInZlciI6MywiYW1yIjpbInB3ZCJdfQ .v2vYQXQGgBDKgY6ggyy4V1Xv_K7aEz2vYQXGgBDKgY6g YCiD8qlNRb_D2Qp4AwC3q0L7j6l-qtEyrpzF7qI4LaWNw6N_MRKaP5m9-Zc9c6q1Q1miX yjFvjBJcwc3f2VdXEa5d49Qg9yHhdi3Y6RbQim8fuz-HR7MexEc94RGf0FS5Rc2EbixlEt kiYtziM9LfIRXskfy-wkUWdrHwwC7A_qQnuMiKIyUfQr0MEP9lH-lMZv6XtB0EapmfP4E wgTIK4Ak_dvzWQEffhyT36QbkmDkHYbQk1if9BcriXXgJgZ0Pz433_ETDgEHlULJg”}');
  地點。重新載入（）；//重新載入網頁
} else  if ( window .confirm ( "網站錯誤，按「確定」來開啟網站。" )) {
  window.open ( ' https : //testbank.hle.com.tw','_blank ' ) ;
@@ -210,27 +188,64 @@ if (window.location.href.startsWith("https://testbank.hle.com.tw")) {
連結：[翰林輔材網] ( https://reference.hle.com.tw )
``` js
if ( window.location.href.startsWith ( “ https://reference.hle.com.tw ” ) ) {
  sessionStorage.setItem("accessToken", “eyJhbGciOiJSUzI1NiIsImtpZCI6Ijg1NzgwNWYxZGQ3ZmE5YTZiNTI3ZjQ0ZWNmZmJkNDhjIiwFMHlwIjot 7YvKu2zsD4t8JoYLtUHeKopyBAb-mxneB3hU0Ejdt_-9iI-4z60_KEAnzLeBp2Gv0SSxpBgFdweRn31MIP4WHGCfpq4rPAGmdIpnWPUBTYywRcpnWPUB F7JOV_23qZIsyfXcj78K_FnBJwGuaT6J4oiyNSmuWjV7mx8tMj0IHINK3C5IJKmDDOX9ymmCk5WQ2mLuckjgel3uWoFxZTwT1mOxrVqGHmgYVo hrrt8f3YJuzLfoHxCmVQ6AW8zdc9OKi4xtaYwhHxjEOHZ5GFZ45uorWRxLIcuukdLLpUgQMl7awnL6yXbT-En7Bxzw-5v8P0WFhSI4tS8bHgSI4tS8bHg”）；
  sessionStorage.setItem("accessToken", “eyJhbGciOiJSUzI1NiIsImtpZCI6Ijg1NzgwNWYxZGQ3ZmE5YTZiNTI3ZjQ0ZWNmZmJkNDhj IiwidHlwIjoiYXQrand0In0.-WwjyIsImlzaWRlbnRpZmllZCI6dHJ1ZSwibG9jayI6ZmFsc2 UsInZlciI6Mywic2NvcGUiOlsib3BlbmlkIiwicHJvZmlsZSIsIm9mZmxpbmVfYWNjZXNzIl0 sImFtciI6WyJwd2QiXX0.xzaLXn13B5pOFPg7k7kOYcrHd3UGm2EIKaGJwHqcXY006ttgVygD O8MfcYMf3grrtgXPjbMZ_esLGu-hZqYb_Ajf_RfRfFtXexLeqeqewBaXWC1va-TrMuxjUCxrW_ByyO1gcNoTdyiuMSITR1TCepX3vEKC44N2ivWF4pDApDpDDpDpD進程進程44445444454pF44pDA4pDApDpkp 0UxfywQQAK_6lu9ifxqq359PvX_I1tnvLVP9hQKe8DfLujVAItPhaGJ-1luV5-UWJt8ooOuRc zYs1bqM5EMsV-iShCdVLvoTYYIaLRVy9dbEA84qRqvd0YE2Bmogat1STmNGRsryfNL66yEw"); // 設定權限
  sessionStorage.setItem("userToken", 「eyJhbGciOiJSUzI1NiIsImtpZCI6Ijg1NzgwNWYxZGQ3ZmE5YTZiNTI3ZjQ0ZWNmZmJkNDhjIiwidHlwIjoiSldUIn0.-WwjyIsImlWRmJjyIsImlJiS6ZmJZxjyIsIml 9jayI6ZmFsc2UsInZlciI6MywiYW1yIjpbInB3ZCJdfQ.TjqNUyWNAq7vhblmsAcAm8S5s-vk4_PuoczKvg1K8yv1W2XAwVWnzPJSvdh4158w -HNx0GVt4XqRn8EoKStyQF_66_i3jr5KsiUIQWlvCZAvm37akA74giYREgEBCG40c765lL0qqXFoVXaQ-Ko89_Qeu3GrfJcEI3yelZ7MRSP 4kMTqj_V0GSTSRTXleawGCQM7vQSgif7ylx5fwUT7O_Hg6mByuPDE9BRPBVweKqZdIzeSTGdjs8Hp87trAfL8RS_QMIJq_rExJc7byOYF9zN-e78_bzN-e // 設置權杖
  會話存儲。setItem ( " userRole " , "老師" ); //將身分設為老師
  地點。重新載入（）；//重新載入網頁
} else  if ( window .confirm ( "網站錯誤，按一下「確定」來開啟翰林輔材網。 " )) {
  window.open ( ' https : //reference.hle.com.tw','_blank ' ) ;
}
```

### ✅翰林教學資源
連結：[翰林教學資源] ( https:// www.hle .com.tw )
### ✅奇鼎事業
連結：[奇鼎事業] ( https:// ebook02.chiding .com.tw /BookCase/publish/index.html )
``` js
if ( window.location.href.startsWith ( “ https://www.hle.com.tw ” ) ) {
  本地儲存。setItem ( "角色" , "老師" ); //將身分設為老師
  localStorage.setItem("令牌", “eyJhbGciOiJSUzI1NiIsImtpZCI6Ijg1NzgwNWYxZGQ3ZmE5YTZiNTI3ZjQ0ZWNmZmJkNDhjIiwidHlFMwIjoiWrandjQ0ZWNmZmJkNDhjIiwidHlFMwIjoiY 7YvKu2zsD4t8JoYLtUHeKopyBAb-mxneB3hU0Ejdt_-9iI-4z60_KEAnzLeBp2Gv0SSxpBgFdweRn31MIP4WHGCfpq4rPAGmdIpnWPUBTYywRcpnWPUB F7JOV_23qZIsyfXcj78K_FnBJwGuaT6J4oiyNSmuWjV7mx8tMj0IHINK3C5IJKmDDOX9ymmCk5WQ2mLuckjgel3uWoFxZTwT1mOxrVqGHmgYVo hrrt8f3YJuzLfoHxCmVQ6AW8zdc9OKi4xtaYwhHxjEOHZ5GFZ45uorWRxLIcuukdLLpUgQMl7awnL6yXbT-En7Bxzw-5v8P0WFhSI4tS8bHgSI4tS8bHg”；
  地點。重新載入（）；//重新載入網頁
} else  if ( window .confirm ( "網站錯誤，按「確定」來開啟網站。" )) {
  window.open ( ' https : //www.hle.com.tw','_blank ' ) ;
if ( window.location.href.startsWith ( “ https://ebook02.chiding.com.tw/BookCase/publish/index.html ” ) ) {
    var執行=  false ;
    document.querySelectorAll ( ' .downAssetBtn ' ) .forEach ( function ( button ) {
      if ( ! executed && ( ! document.getElementById ( ' assetsPage ' ) || document.getElementById ( ' assetsPage ' ) . style.display === ' none ' ) ) {   
        alert ( '請先點選您要使用的電子書，再執行指令碼。' );
        已執行= 真；
      } else  if（！執行）{
        var link =  document.createElement ( ' a ' ) ;
          link.href = ' https://ebook02.chiding.com.tw/EbookViewer/publish/Ebook.html?id= ' + ( button.getAttribute ( ' d - file_name ' ) ? button.getAttribute ( ' d -  file_name ' ) .replace ( ' . ) ' , ' ) : '​​​    
          關聯。textContent  =  '開啟' ;
        按鈕.innerHTML = ' ' ;  
        按鈕.appendChild (連結)；
        本地儲存。setItem ( "登入帳號" , "模擬帳號" ); //設定假帳號
        本地儲存。setItem ( “ uuid ” , “ mockUUID ” ); //設定假UUID
  }})}
```
>最後測試時間：2024/9/22
</詳情>
### ❌ 目前無效
<詳細資料>
    <summary>按這裡展開</summary>

### ❌康軒總複習即測卷
連結：[康軒總複習即測卷] ( https://ttrplatform.knsh.com.tw/teacher )
``` js
if ( window.location.href.startsWith ( “ https://ttrplatform.knsh.com.tw/ ” ) ) {
  文件. cookie = “ connect.sid=s%3AXM5bGeC2DRBIbxOybL3jxaUHrWUhone4.L298aSJXZtxyUyXBV6UTk4I5rYoWAJ0OYi1VyTfl% 2BXs ”  ； 
  視窗.位置.href = “ https://ttrplatform.knsh.com.tw/teacher ” ;  
} else  if ( window .confirm ( "網站錯誤，按一下「確定」來開啟翰林行動大師。" )) {
  window.open ( ' https://ttrplatform.knsh.com.tw/teacher','_blank ' ) ;
}
```

>最後測試時間：2024/5/23
### ❌何嘉仁電子書
連結：[何嘉仁電子書櫃] ( https://bookonline.hess.com.tw/bookcase/#/ )
``` js
if ( window.location.href.startsWith ( “ https://bookonline.hess.com.tw/bookcase/#/ ” ) ) {
if ( ! localStorage.getItem ( " isLogin " ) ) {
  本地儲存。setItem ( “ isLogin ” , “ true ” ); //將登入狀態設為true
  本地儲存。setItem ( " uuid " , " mock_user " ); //設定假的教師UUID
  地點。重新載入（）；//重新載入網頁
}} else  if ( window .confirm ( "網站錯誤，按一下「確定」來開啟何嘉仁電子書。" )) {
  window.open ( ' https://bookonline.hess.com.tw/bookcase/#/','_blank ' ) ;
}
```
</詳情>

##可用帳號
@@ -285,19 +300,19 @@ if (window.location.href.startsWith("https://www.hle.com.tw")) {
-感謝** <ins> @foxvegajian </ins> **提供康軒網頁媒體盒的下載方法。 ( [原訊息] ( https://gist.github.com/aliyaliu368/891eef75e09494e965d291ead4a80d17?permalink_comment_id=4685986#gistcomment-4685986 ) ）
-感謝** <ins> @ J56tw </ins> **提供康軒電子書的免登入方法。( [原訊息] ( https://gist.github.com/notlin4/a05d7db77cd5606a812f4b9900fef3ee?permalink_comment_id=4788981#gistcomment-4788981 )）
-感謝** < ins > @ tmyrhs3 </ ins > **提供翰林帳號。 （[原訊息] ( https://gist.github.com/notlin4/a05d7db77cd5606a812f4b9900fef3ee?permalink_comment_id=4814684#gistcomment-4814684 )）
-趕寫** <ins> @小哲<ins>提供奇鼎事業的免登入方法（Discord ）
-最後感謝所有回答別人問題的人！

如果你覺得這篇教學對你有幫助，請點選本篇教學最上方的星星圖標，支持我繼續製作下去！

##限制
-因為本指令碼在少數網站上僅繞過了驗證，因此可能會導致無法使用儲存資料記錄、修改等功能。
-翰林版電子書每天會自動重設數據，因此需重新執行指令碼。
-翰林版電子書將於2024/6/30新增翰林帳號驗證，未來此破解方法可能無法使用，須尋找更好的解決方案。
-現有的一些指令碼有些地方的迴避方式不太好，將來也許可以用其他方式執行指令碼來交換編碼行為。

---

腳本由[ SiongSng ] ( https://github.com/SiongSng )製作，由[ notlin4 ] ( https://github.com/notlin4 )繼續| 本指令代碼由[菘菘]   ( https://github.com/SiongSng )製作，由[ notlin4 ] ( https://github.com/SiongSng )製作，由[ notlin4 ] ( https://notubub.com/not 4ub ) .
版權所有 © 2022-2024 [菘菘] ( https://github.com/SiongSng )和[ notlin4 ] ( https://github.com/notlin4 )。版權所有，並一切保留權利。  
版權所有 © 2022-2024 [菘菘] ( https://github.com/SiongSng )和[ notlin4 ] ( https://github.com/notlin4 )。保留所有權利。
版權所有 © 2022-2024 [ SiongSng ] ( https://github.com/SiongSng )和[ notlin4 ] ( https://github.com/notlin4 )。保留所有權利。
![ ] ( https://hit.yhype.me/github/profile?user_id=121224522 ) <!--觀看次數追蹤 https://yhype.me/github/profile-views -->
@notlin4 notlin4 修改了 這個要點2024年7月2日。
 修改了 1 個文件 ，新增 13 處 ， 刪除 13 處。
 26 處修改：13 處新增 & 13 處刪除二十六 
without-auth_e-book_tutorial_免登錄電子書教學.md
原始文件行號	不同行號	差異線變化
@@ -1,6 +1,6 @@
#教學用電子書及相關工具免登教學

**使用本指令碼即代表您同意本[免責聲明] ( #免責聲明)。**
**使用本指令碼即表示您同意《[免責聲明] ( #免責聲明) 》。**

##免責聲明
###將請勿將本指令碼作為抄襲答案、指向等惡意目的，使用本指令碼，請「自行承擔」一切後果與風險。
@@ -48,7 +48,​​7 @@ javascript:(function(){var script=document.createElement('script');script.src='h

###主機版
1 .前往要使用的電子書或相關工具網站。
2.按F12開啟開發人員工具，然後切換到主控台（Console）分頁。
2 .按F12開啟開發人員工具，然後切換到主控台( Console )分頁。
3 .貼上以下指令碼並執行：
``` javascript
javascript :( function ( ) { var script = document . createElement ( ' script ' ) ; script . src = ' https://cdn.jsdelivr.net/gh/notlin4/without-auth_e-book@main/fast.js '​​​​​
@@ -58,13 +58,13 @@ javascript:(function(){var script=document.createElement('script');script.src='h

![繁體中文] ( https://gist.github.com/assets/121224522/f1e71739-7a86-465b-bae5-965fcef6d23c )

如果您使用的是繁體中文（如上圖），請輸入「`允許貼上`」，然後按 Enter鍵。
如果你使用的是允許繁體中文（如上圖），請在控制台輸入「`允許貼上` ”，然後按 Enter鍵貼上。

![中文] ( https://gist.github.com/assets/121224522/11aa0d00-3684-4b16-b98a-7c0a6deff90b )

如果您使用的是英文（如上圖），請輸入「`允許貼上`」，然後按Enter鍵。
如果你使用的是中文（如上圖），請在控制台輸入「`允許貼上`」，並按下Enter鍵允許貼上。

其他語言，請輸入對應引號中的內容，然後按下Enter鍵。
對於其他語言，請在控制台輸入對應中的內容，並按下Enter鍵允許貼上。
</詳情>

4 .達成交付登錄！
@@ -75,23 +75,23 @@ javascript:(function(){var script=document.createElement('script');script.src='h

###指令碼版本
<詳細資料>
    <summary>進一步展開</summary>
    <summary>按這裡展開</summary>

1 .前往要使用的電子書或相關工具網站。
2.按F12開啟開發人員工具，然後切換到主控台（Console）分頁。
2 .按F12開啟開發人員工具，然後切換到主控台( Console )分頁。
3 .貼上下方的指令碼並執行。
<詳細資料>
    <summary>無法貼上嗎？在這裡查看如何修改</summary>

![繁體中文] ( https://gist.github.com/assets/121224522/f1e71739-7a86-465b-bae5-965fcef6d23c )

如果您使用的是繁體中文（如上圖），請輸入「`允許貼上`」，然後按 Enter鍵。
如果你使用的是允許繁體中文（如上圖），請在控制台輸入「`允許貼上` ”，然後按 Enter鍵貼上。

![中文] ( https://gist.github.com/assets/121224522/11aa0d00-3684-4b16-b98a-7c0a6deff90b )

如果您使用的是英文（如上圖），請輸入「`允許貼上`」，然後按Enter鍵。
如果你使用的是中文（如上圖），請在控制台輸入「`允許貼上`」，並按下Enter鍵允許貼上。

其他語言，請輸入對應的內容，然後按下Enter鍵。
對於其他語言，請在控制台輸入對應中的內容，並按下Enter鍵允許貼上。
</詳情>

4 .達成交付登錄！
@@ -104,7 +104,7 @@ if (window.location.href.startsWith("https://webetextbook.knsh.com.tw/")) {
  var執行=  false ;
  document.querySelectorAll ( ' .downAssetBtn ' ) .forEach ( function ( button ) {
    if ( ! executed && ( ! document.getElementById ( ' assetsPage ' ) || document.getElementById ( ' assetsPage ' ) . style.display === ' none ' ) ) {   
      alert ( '請先點選你要使用的電子書再執行指令碼。' );
      alert ( '請先點選您要使用的電子書，再執行指令碼。' );
      已執行= 真；
    } else  if ( ! executed &&  button .getAttribute ( ' d - title ' ) .includes ( " (網頁版) " )) {
      alert ( '偵測到一到五年級的內容，目前不支持繞過一到五年級的電子書，請改用網頁媒體盒進行下載。造成不便之處，我們見諒。' );
@@ -164,7 +164,7 @@ if (window.location.href.startsWith("https://edisc3.hle.com.tw/edisc_v3")) {
if ( window.location.href.includes ( “ oneclass.com.tw ” ) ) {
  讓mockToken =  JSON.stringify ( {
  “代碼”： “成功”，
  jwt ：eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJpc3MiOiJodHRwOi8vbXlhY2NvdW50Lm5hbmkuY29vbC8iLCJzdWI iOiJ1c2Vycy9rb2xhZGkxNzYyIiwiZnJvbSI6Ik5hbmkiLCJ1c2VybmFtZSI6ImtvbGFkaTE3NjIiLCJlbWFpbHZhbGl kIjp0cnVlLCJtb2JpbGV2YWxpZCI6ZmFsc2UsImVtYWlsIjoia29sYWRpMTc2MkBidXpibG94LMNvbSIsInVpZCI ​6ImZiZDY2Y2YwLTA2ZjYtMTFlZi1iNmUyLWJmYWI3YjYwOGJiMiIsImp0aSI6Ijk2YWE0ZjYzLThmYzMtNGEzMS1iMjIz LTk3YjIxZWU5NmNlNCIsImlhdCI6MTcxNDQ4NDM5MywiZXhwIjoxNzE5NjY4MzkzfQ.IG9QpMa28e2yTEBPxhtOZy3VXSAsF77KmFsRNsSo_9k ” }); 
  jwt ：eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJpc3MiOiJodHRwOi8vbXlhY2NvdW50Lm5hbmkuY29vbC8iLCJzd WIiOiJ1c2Vycy91bmljeWNsZTQiLCJmcm9tIjoiTmFuaSIsInVzZXJuYW1lIjoidW5pY3ljbGU0IiwiZW1haWx2YWxp ZCI6dHJ1ZSwibW9iaWxldmFsaWQiOmZhbHNlLCJlbWFpbCI6ImtyNTJ5NTRtQGR1Y2suY29tIiwidWlkIjoiND​ A3YzBhNjAtMzgxZS0xMWVmLWEyZjMtMGYxNmE0Y2MyYjA4IiwianRpIjoiY2FjNDAzYjAtZjkyYS00YmY1LTg0MDktN WM1OTk1OGEwMTIxIiwiaWF0IjoxNzE5ODg4ODQzLCJleHAiOjE3MjUwNzI4NDN9.-usPxm8q72YvcAkqqdRSYoxVC-h2K862EV8DCtMZQCI “ ); 
  讓欄位名稱=  " nani_oneclass_login_token " ;
  var d =  new  Date ();
  d . setTime ( d.getTime () + ( 1 * 24 *  60 * 60 * 1000  ) ) ;      
@@ -284,7 +284,7 @@ if (window.location.href.startsWith("https://www.hle.com.tw")) {
-感謝** [菘菘] ( https://github.com/SiongSng ) **製作了原始教學。 （[原教學] ( https://gist.github.com/SiongSng/baa4f015258d0312f627b5659d93d72e )已刪除，原始內容[文件] ( https://gist.github.com/tom Cheng1111/ 3c647b6b09 )於 2022/2/1），請參閱常見問題第 1 項）
-感謝** <ins> @foxvegajian </ins> **提供康軒網頁媒體盒的下載方法。 ( [原訊息] ( https://gist.github.com/aliyaliu368/891eef75e09494e965d291ead4a80d17?permalink_comment_id=4685986#gistcomment-4685986 ) ）
-感謝** <ins> @ J56tw </ins> **提供康軒電子書的免登入方法。( [原訊息] ( https://gist.github.com/notlin4/a05d7db77cd5606a812f4b9900fef3ee?permalink_comment_id=4788981#gistcomment-4788981 )）
- ** < ins > @ tmyrhs3 </ ins > ** 提供康軒總複習即測卷、翰林和南一帳號。 （感謝[原消息] ( https://gist.github.com/notlin4/a05d7db77cd5606a812f4b9900fef3ee?permalink_comment_id=4814684#gistcomment-4814684 )）
-感謝** < ins > @ tmyrhs3 </ ins > ** 提供翰林帳號。 （[原訊息] ( https://gist.github.com/notlin4/a05d7db77cd5606a812f4b9900fef3ee?permalink_comment_id=4814684#gistcomment-4814684 )）
-最後感謝所有回答別人問題的人！

如果你覺得這篇教學對你有幫助，請點選本篇教學最上方的星星圖標，支持我繼續製作下去！
@notlin4 notlin4 修改了 這個要點2024年7月2日。
 修改了 1 個文件 ，其中 新增 5 項 ， 刪除 9 項。
 14 處修改：5 處添加，9 處刪除14 
without-auth_e-book_tutorial_免登錄電子書教學.md
原始文件行號	不同行號	差異線變化
@@ -54,7 +54,7 @@ javascript:(function(){var script=document.createElement('script');script.src='h
javascript :( function ( ) { var script = document . createElement ( ' script ' ) ; script . src = ' https://cdn.jsdelivr.net/gh/notlin4/without-auth_e-book@main/fast.js '​​​​​
```
<詳細資料>
    <summary>無法貼上嗎？點我看如何修復</summary>
    <summary>無法貼上嗎？在這裡查看如何修改</summary>

![繁體中文] ( https://gist.github.com/assets/121224522/f1e71739-7a86-465b-bae5-965fcef6d23c )

@@ -81,7 +81,7 @@ javascript:(function(){var script=document.createElement('script');script.src='h
2 .按F12開啟開發人員工具，然後切換到主控台（Console）分頁。
3 .貼上下方的指令碼並執行。
<詳細資料>
    <summary>無法貼上嗎？點我看如何修復</summary>
    <summary>無法貼上嗎？在這裡查看如何修改</summary>

![繁體中文] ( https://gist.github.com/assets/121224522/f1e71739-7a86-465b-bae5-965fcef6d23c )

@@ -241,17 +241,13 @@ if (window.location.href.startsWith("https://www.hle.com.tw")) {
-密碼：` koladi1762 `

**南一**
-頭像：` Saddled7129`
-密碼：` Saddled7129`

**康軒總複習即測卷**
-帳號：` ramaw19340 `
-密碼：` a1b2c3d4 `
-帳號：`獨輪車4`
-密碼：` unicycle4`

##常見問題
**你可以在留言區提問，但在提問前請先看這裡！**
<詳細資料>
    <summary>進一步展開</summary>
    <summary>按這裡展開</summary>

1 .為什麼具體的教學不見了？
>作者本教學為因果的分支（Fork）版本，原[菘菘] ( https://github.com/SiongSng )已刪除原教學，若要查看原因請點選下方「查看原因」來展開，也請各位不要討論版權法或出版商規範的話題。
@notlin4 notlin4 修改了 這個要點2024年6月18日。
 修改了 1 個文件 ， 新增了 2 處 ， 刪除了 2 處。
 4 處修改：2 處新增 & 2 處刪除4 
without-auth_e-book_tutorial_免登錄電子書教學.md
原始文件行號	不同行號	差異線變化
@@ -241,8 +241,8 @@ if (window.location.href.startsWith("https://www.hle.com.tw")) {
-密碼：` koladi1762 `

**南一**
-帳號：` koladi1762 `
-密碼：` koladi1762 `
-頭像：` Saddled7129`
-密碼：` Saddled7129`

**康軒總複習即測卷**
-帳號：` ramaw19340 `
@notlin4 notlin4 修改了 這個要點2024年5月23日。
 修改了 1 個文件 ，新增 27 項 ， 刪除 12 項。
 39 處修改：27 處添加，12 處刪除三十九 
without-auth_e-book_tutorial_免登錄電子書教學.md
原始文件行號	不同行號	差異線變化
@@ -132,6 +132,17 @@ if (window.location.href.startsWith("https://webetextbook.knsh.com.tw/")) {
}
```

### ✅康軒總複習即測卷
連結：[康軒總複習即測卷] ( https://ttrplatform.knsh.com.tw/teacher )
``` js
if ( window.location.href.startsWith ( “ https://ttrplatform.knsh.com.tw/ ” ) ) {
  文件. cookie = “ connect.sid=s%3AXM5bGeC2DRBIbxOybL3jxaUHrWUhone4.L298aSJXZtxyUyXBV6UTk4I5rYoWAJ0OYi1VyTfl% 2BXs ”  ； 
  視窗.位置.href = “ https://ttrplatform.knsh.com.tw/teacher ” ;  
} else  if ( window .confirm ( "網站錯誤，按一下「確定」來開啟翰林行動大師。" )) {
  window.open ( ' https://ttrplatform.knsh.com.tw/teacher','_blank ' ) ;
}
```

### ✅ 翰林電子書
連結：[翰林行動大師] ( https://edisc3.hle.com.tw/edisc_v3/ebook_v2023.html )  
``` js
@@ -140,7 +151,7 @@ if (window.location.href.startsWith("https://edisc3.hle.com.tw/edisc_v3")) {
  本地儲存。setItem ( “ last_signinX_v2023 ” ,時間); //將帳號登錄日期設定為目前時間，避免被取代為過渡
  本地儲存。setItem ( " roleX_v2023 " , "老師" ); //將身分設為老師
  本地儲存。setItem ( " emailX_v2023 " , " test@test.com " ); //由於翰林電子書會驗證是否有設定郵件，只要設定即可使用
  localStorage。 O0cOsie3P40svSZXhhpNkvt-uZpdkZctVI4rl_SCYdBzniZjf25QaBRUIo0C9EHbHWOdk7G3hQ-gvwndFiz7ukku3r7pLJ97V_F-pqMWgvIgv IDrTPK0SRTYxTozhDTUXdJ20VsFQMOFbm466f2a0i6QJ4PXEjFak-qAZabOvrtG1Nuygc23xsMiDPjKdT9CnAy-biMyb-bN8CiIVECqpbFBk 45ap-1Ke_5e4pHA958vAbC9ti1aqzMCNqMyy3KwGaMitRlRM_kJ9krTB587_5ewd0GFFaiqX2jwaKZBGVJnBosrMU38d6Edue9puwMLm4TdgX2jwaKZBGVJnBosrMU38d6Edue9puwMLm4TdgX2jwaKZBGVJnBosrMU38d6Edue9puwMLm4TdgX2jwaKZBGVJnBosrMU38d6Edue9puwMLm4Tdg”）； // 設定驗證用的權限
  localStorage.setItem("tokenX_v2023", “eyJhbGciOiJSUzI1NiIsImtpZCI6Ijg1NzgwNWYxZGQ3ZmE5YTZiNTI3ZjQ0ZWNmZmJkNDhjjIiwidlw. 7YvKu2zsD4t8JoYLtUHeKopyBAb-mxneB3hU0Ejdt_-9iI-4z60_KEAnzLeBp2Gv0SSxpBgFdweRn31MIP4WHGCfpq4rPAGmdIpnWPUBTYywRcpnWPUB F7JOV_23qZIsyfXcj78K_FnBJwGuaT6J4oiyNSmuWjV7mx8tMj0IHINK3C5IJKmDDOX9ymmCk5WQ2mLuckjgel3uWoFxZTwT1mOxrVqGHmgYVo hrrt8f3YJuzLfoHxCmVQ6AW8zdc9OKi4xtaYwhHxjEOHZ5GFZ45uorWRxLIcuukdLLpUgQMl7awnL6yXbT-En7Bxzw-5v8P0WFhSI4tS8bHgSI4tS8bHg”；
  地點。重新載入（）；//重新載入網頁
} else  if ( window .confirm ( "網站錯誤，按一下「確定」來開啟翰林行動大師。" )) {
  window.open ( ' https://edisc3.hle.com.tw/edisc_v3/ebook_v2023.html','_blank ' ) ;
@@ -153,7 +164,7 @@ if (window.location.href.startsWith("https://edisc3.hle.com.tw/edisc_v3")) {
if ( window.location.href.includes ( “ oneclass.com.tw ” ) ) {
  讓mockToken =  JSON.stringify ( {
  “代碼”： “成功”，
  jwt ：eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJpc3MiOiJodHRwOi8vbXlhY2NvdW50Lm5hbmkuY29vbC8iLCJzdW IiOiJ1c2Vycy93aXRob3V0YXV0aCIsImZyb20iOiJOYW5pIiwidXNlcm5hbWUiOiJ3aXRob3V0YXV0aCIsImVtYWlsdm FsaWQiOnRydWUsIm1vYmlsZXZhbGlkIjpmYWxzZSwiZW1haWwiOiJiOWo3OWEyZ0BkdWNrLmNvbSIsInVpZCI6I ​jczOTAxNWIwLWU3OTUtMTFlZS05NGVkLWI5ZDJmNjk5NGQyZCIsImp0aSI6ImJkNTdlYzEzLTNiZDEtNDM5OS1hNTNlL TkyNzVhNDNkYzJlYyIsImlhdCI6MTcxMTAzNDAxMiwiZXhwIjoxNzE2MjE4MDEyfQ.bHi4mgrDaxlsODByZtdEWzUG17KPixEnlVoIzR2twVYY } ); 
  jwt ：eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJpc3MiOiJodHRwOi8vbXlhY2NvdW50Lm5hbmkuY29vbC8iLCJzdWI iOiJ1c2Vycy9rb2xhZGkxNzYyIiwiZnJvbSI6Ik5hbmkiLCJ1c2VybmFtZSI6ImtvbGFkaTE3NjIiLCJlbWFpbHZhbGl kIjp0cnVlLCJtb2JpbGV2YWxpZCI6ZmFsc2UsImVtYWlsIjoia29sYWRpMTc2MkBidXpibG94LMNvbSIsInVpZCI ​6ImZiZDY2Y2YwLTA2ZjYtMTFlZi1iNmUyLWJmYWI3YjYwOGJiMiIsImp0aSI6Ijk2YWE0ZjYzLThmYzMtNGEzMS1iMjIz LTk3YjIxZWU5NmNlNCIsImlhdCI6MTcxNDQ4NDM5MywiZXhwIjoxNzE5NjY4MzkzfQ.IG9QpMa28e2yTEBPxhtOZy3VXSAsF77KmFsRNsSo_9k ” }); 
  讓欄位名稱=  " nani_oneclass_login_token " ;
  var d =  new  Date ();
  d . setTime ( d.getTime () + ( 1 * 24 *  60 * 60 * 1000  ) ) ;      
@@ -177,7 +188,7 @@ if (window.location.href.includes("oneclass.com.tw")) {
``` js
if ( window.location.href.startsWith ( “ https://bookonline.hess.com.tw/bookcase/#/ ” ) ) {
if ( ! localStorage.getItem ( " isLogin " ) ) {
  本地儲存。setItem ( “ isLogin ” , “ true ” ); // 將登入狀態設為（ true ）
  本地儲存。setItem ( “ isLogin ” , “ true ” ); // 將登入狀態設為true
  本地儲存。setItem ( " uuid " , " mock_user " ); //設定假的教師UUID
  地點。重新載入（）；//重新載入網頁
}} else  if ( window .confirm ( "網站錯誤，按一下「確定」來開啟何嘉仁電子書。" )) {
@@ -189,7 +200,7 @@ if (!localStorage.getItem("isLogin")) {
連結：[翰林雲端命題大師] ( https://testbank.hle.com.tw )
``` js
if ( window.location.href.startsWith ( “ https://testbank.hle.com.tw ” ) ) {
  localStorage.setItem("oidc.user:https://id.hle.com.tw:js", '{“access_token”：“eyJhbGciOiJSUzI1NiIsImtpZCI6Ijg1NzgwNWYxZGQ3ZmE5YTZiNTI3ZjQ0ZWNmZmJkNDhjIiwidHlwIjoiNTI3ZjQ0ZWNmZmJkNDhjIiwidHlwIjoiYXQQ5901ZFXQ59 OISwQo99RwPj0mTHnb9Aod2_hDKuzqvxSXO4sIcuzNesa8WcoAJUd3ZdIgsPlIpFGxuioN xEsbWbm-sR9tv-OQUdiEuAXSAkiB_-1y5TKeUbF_nDxQ-KjwjAiwkaLqyXA2cGcpX3j2F7v J5fU8rkEqmHyjMeoRV25Qc3cqSQfqmzTbZnLfJzS7tnM00zoIPrb9NPIKnMTm0LNipFd_u AzxCGQzsal0Gyxm5Hd45Hjk4GFu2fPtOtq2U4bBjKcaRljD8LwUhMFZH_PGkuOxncZHvS8h c-Lx9YS3QgQDuOELKc6UgRsMZ7008ql7uA","id_token":"eyJhbGciOiJSUzI1NiIsIm tpZCI6Ijg1NzgwNWYxZGQ3ZmE5YTZiNTI3ZjQ0ZWNmZmJkNDhjIiwidHlwIjoiSldUIn0..PK3xCNkOkgHw-peD_QwuWH7XlPJCiMCdX5QFh_clfh31km-Bl9uLxvEkqO4VSpGgP2ZUSyoU0Y1D-xzi44Rmjy lv0GJcuIViAyU_5UgyjpxJFtB0J8NDzegnIenr3QzJPOqItWA7y4BkMMp79gjNtBwU3kEuMliIYqgdaM_pEZB_G 8nnU_1moaI-drcHejk-p_GynCmJl2HMfquxwRR66d5g9QXdYm08x3491J6COdAKgMej7mNt6Z4GnMKMamIx7gJA Dre3Hd563qHWBxSmj9MGPkl9xEvKWAEMU_jg_A6KNQICUb-B0YfD3sh4IqLi5ZkPIGZV1EuKNUoxLE6Kpw”}');
  localStorage.setItem("oidc.user:https://id.hle.com.tw:js", '{“access_token”：“eyJhbGciOiJSUzI1NiIsImtpZCI6Ijg1NzgwNWYxZGQ3ZmE5YTZiNTI3ZjQ0ZWNmZmJkNDhjIiwidHlwIjoiYXQrand0In0iYXQrand0In0 ..tRzJFMcjaxDj7YvKu2zsD4t8JoYLtUHeKopyBAb-mxneB3hU0Ejdt_-9iI-4z60_KEAnzLeBp2Gv0SSxpBgFdweRn31MIP4WHGCfpqLeBp2Gv0SSxpBgFdweRn31MIP4WHGCfpq4rPAGImd WPUBTYywRcXF7JOV_23qZIsyfXcj78K_FnBJwGuaT6J4oiyNSmuWjV7mx8tMj0IHINK3C5IJKmDDOX9ymmCk5WQ2mLuckjglel3uWoFxZTwT1mOx qGHmgYVohrrt8f3YJuzLfoHxCmVQ6AW8zdc9OKi4xtaYwhHxjEOHZ5GFZ45uorWRxLIcuukdLLpUgQMl7awnL6yXbT-En7Bxzw-5v8P0WFhSI4tS8b Hg","id_token":"eyJhbGciOiJSUzI1NiIsImtpZCI6Ijg1NzgwNWYxZGQ3ZmE5YTZiNTI3ZjQ0ZWNmZmJkNDhjIiwidHlwIjoiNTI3ZjQ0ZWNmZmJkNDhjIiwidHlwIjoiSldUIn0..cySod WB702wd4_IXGXWuwcas0m7jUL2VSCUnmHcTWKpNy7GPZTJv5FjMHVISwpViS8pxrWnKzd0YA3xCAopo7XB0_n1W8OjPb82dALd4nt-9xCAopo7XB0_n1W8OjPb82dALd4nt-9ozP0IedAOEo ji_2XoTf-TtBSCtsOFa6H6WZtRG4In8v-8fVLYrBVTdVs9mSiGAn_W7GQiI-fhbb6G3MM3ctKoPLg-0LmVELDbp0gFKNUbIQhpxIKS3M3ctIkpl3-f 2mT9OiGlgFieY6xhNpSyPCqnFA7HSvMHfJFYlgOfU2RdEJyZQSitbLYEsh-vNZrufrewpxW6Bdc4AqI4U_KXOrOoo1T7TowBWOg7dxLPHhw}'');
  地點。重新載入（）；//重新載入網頁
} else  if ( window .confirm ( "網站錯誤，按「確定」來開啟網站。" )) {
  window.open ( ' https : //testbank.hle.com.tw','_blank ' ) ;
@@ -199,7 +210,7 @@ if (window.location.href.startsWith("https://testbank.hle.com.tw")) {
連結：[翰林輔材網] ( https://reference.hle.com.tw )
``` js
if ( window.location.href.startsWith ( “ https://reference.hle.com.tw ” ) ) {
  sessionStorage.setItem("accessToken", “eyJhbGciOiJSUzI1NiIsImtpZCI6Ijg1NzgwNWYxZGQ3ZmE5YTZiNTI3ZjQ0ZWNmZmJkNDhjIiwidHlwIjoiwidHw; PPq5wOhITi3TRddTqfWq-_yHWAPf0jw9EYNWE2LTT7lkTBET-RO6dXSOOR9E7eHeXlaxwPCGKErK0JJYY_WxvgxmuARub2YiAmS2zYsHoIpBCE5 yMFkjw2HKKFQ4nMf_pQj8bazx6aYEFGRYL8K1vC8Y2omugd3igVbqF6IE7wjBg35CLiLt20aYpVYaNE8mikoCQjQ3BMIuuf_h0e61N5ZqqRUN lbJj-kjILJ2UjQ8x_5woE5ZB0kh6CJO-34ygGHcd7G17XUbuJY_Y-vuldpqexlo43SUDVmgkDiF1HkJuoEGQtzbV6auhqSHpRapN6ktJw7kw"); // 設置權杖
  sessionStorage.setItem("accessToken", “eyJhbGciOiJSUzI1NiIsImtpZCI6Ijg1NzgwNWYxZGQ3ZmE5YTZiNTI3ZjQ0ZWNmZmJkNDhjIiwFMHlwIjot 7YvKu2zsD4t8JoYLtUHeKopyBAb-mxneB3hU0Ejdt_-9iI-4z60_KEAnzLeBp2Gv0SSxpBgFdweRn31MIP4WHGCfpq4rPAGmdIpnWPUBTYywRcpnWPUB F7JOV_23qZIsyfXcj78K_FnBJwGuaT6J4oiyNSmuWjV7mx8tMj0IHINK3C5IJKmDDOX9ymmCk5WQ2mLuckjgel3uWoFxZTwT1mOxrVqGHmgYVo hrrt8f3YJuzLfoHxCmVQ6AW8zdc9OKi4xtaYwhHxjEOHZ5GFZ45uorWRxLIcuukdLLpUgQMl7awnL6yXbT-En7Bxzw-5v8P0WFhSI4tS8bHgSI4tS8bHg”）；
  會話存儲。setItem ( " userRole " , "老師" ); //將身分設為老師
  地點。重新載入（）；//重新載入網頁
} else  if ( window .confirm ( "網站錯誤，按一下「確定」來開啟翰林輔材網。 " )) {
@@ -208,29 +219,33 @@ if (window.location.href.startsWith("https://reference.hle.com.tw")) {
```

### ✅ 翰林教學資源
連結：[翰林教學資源] ( https://www.hle.com.tw / )
連結：[翰林教學資源] ( https://www.hle.com.tw )
``` js
if ( window.location.href.startsWith ( “ https://www.hle.com.tw ” ) ) {
  本地儲存。setItem ( "角色" , "老師" ); //將身分設為老師
  localStorage.setItem("令牌", “eyJhbGciOiJSUzI1NiIsImtpZCI6Ijg1NzgwNWYxZGQ3ZmE5YTZiNTI3ZjQ0ZWNmZmJkNDhjIiwidHlwIjoiwidHlwIjoi_pmg00Q 2JXixdy2GFjKIREMBZqXWgu6uAsqk-HsAV_Hl8hW5OSH0lGZ9Gp4csGJcmN-JYip-8T0ZQG22QhXgsHc3wjCd-LJ7Z00w8DNmiQG22QhXgsHc3wjCd-LJ7Z00w8DNmimiQG22QhXgsHc3wjCd-LJ7Z00w8DNmimiwww. MVKTNSsDO2I9gCZAd0BOPYpCNFXzY6TTwH6V2hKW6XJ2RvO2uq-UmeSe-lpXVFaRJ5zohoP2bnn29HSJIwDh-wyroBVIz_2uEorj2Zi8PPcBb4A Ie4Co8X3F1sQYNMzNnxjlKLpfuQpBxt3bzIPAd9XFP6h_21pzVfB4bd6JSQNX3KJ8y0t0KWzWyIBhKf7UuB69q7RXzpgg2BXVclpzpg2BXGlp7
  localStorage.setItem("令牌", “eyJhbGciOiJSUzI1NiIsImtpZCI6Ijg1NzgwNWYxZGQ3ZmE5YTZiNTI3ZjQ0ZWNmZmJkNDhjIiwidHlFMwIjoiWrandjQ0ZWNmZmJkNDhjIiwidHlFMwIjoiY 7YvKu2zsD4t8JoYLtUHeKopyBAb-mxneB3hU0Ejdt_-9iI-4z60_KEAnzLeBp2Gv0SSxpBgFdweRn31MIP4WHGCfpq4rPAGmdIpnWPUBTYywRcpnWPUB F7JOV_23qZIsyfXcj78K_FnBJwGuaT6J4oiyNSmuWjV7mx8tMj0IHINK3C5IJKmDDOX9ymmCk5WQ2mLuckjgel3uWoFxZTwT1mOxrVqGHmgYVo hrrt8f3YJuzLfoHxCmVQ6AW8zdc9OKi4xtaYwhHxjEOHZ5GFZ45uorWRxLIcuukdLLpUgQMl7awnL6yXbT-En7Bxzw-5v8P0WFhSI4tS8bHgSI4tS8bHg”；
  地點。重新載入（）；//重新載入網頁
} else  if ( window .confirm ( "網站錯誤，按「確定」來開啟網站。" )) {
  window.open ( ' https : //www.hle.com.tw','_blank ' ) ;
}
```

>最後測試時間：2024/ 3/21
>最後測試時間：2024/ 5/23
</詳情>
##可用帳號
**請勿更改以下所有帳號的個人資料！**

**翰林**
-帳號：` ramaw19340@wikfee .com `
-密碼：` a1b2c3d4 `
-帳號：` koladi1762@buzblox .com `
-密碼：` koladi1762 `

**南一**
-頭像：` Saddled7129`
-帳號：` koladi1762 `
-密碼：` koladi1762 `

**康軒總複習即測卷**
-帳號：` ramaw19340 `
-密碼：` a1b2c3d4 `

##常見問題
@@ -273,7 +288,7 @@ if (window.location.href.startsWith("https://www.hle.com.tw")) {
-感謝** [菘菘] ( https://github.com/SiongSng ) **製作了原始教學。 （[原教學] ( https://gist.github.com/SiongSng/baa4f015258d0312f627b5659d93d72e )已刪除，原始內容[文件] ( https://gist.github.com/tom Cheng1111/ 3c647b6b09 )於 2022/2/1），請參閱常見問題第 1 項）
-感謝** <ins> @foxvegajian </ins> **提供康軒網頁媒體盒的下載方法。 ( [原訊息] ( https://gist.github.com/aliyaliu368/891eef75e09494e965d291ead4a80d17?permalink_comment_id=4685986#gistcomment-4685986 ) ）
-感謝** <ins> @ J56tw </ins> **提供康軒電子書的免登入方法。( [原訊息] ( https://gist.github.com/notlin4/a05d7db77cd5606a812f4b9900fef3ee?permalink_comment_id=4788981#gistcomment-4788981 )）
-感謝** < ins > @ tmyrhs3 </ ins > ** 提供翰林與南一帳號。 （[原訊息] ( https://gist.github.com/notlin4/a05d7db77cd5606a812f4b9900fef3ee?permalink_comment_id=4814684#gistcomment-4814684 )）
- ** < ins > @ tmyrhs3 </ ins > ** 提供康軒總複習即測卷、翰林和南一帳號。 （感謝[原消息] ( https://gist.github.com/notlin4/a05d7db77cd5606a812f4b9900fef3ee?permalink_comment_id=4814684#gistcomment-4814684 )）
-最後感謝所有回答別人問題的人！

如果你覺得這篇教學對你有幫助，請點選本篇教學最上方的星星圖標，支持我繼續製作下去！
@notlin4 notlin4 修改了 這個要點2024年4月13日。
 修改了 1 個文件 ，新增 13 處 ， 刪除 13 處。
 26 處修改：13 處新增 & 13 處刪除二十六 
without-auth_e-book_tutorial_免登錄電子書教學.md
原始文件行號	不同行號	差異線變化
@@ -13,7 +13,7 @@
開發這個並不是希望拿真正的抄答案，是希望讓需要用的人可以使用，也希望各家出版社能夠提供一個學生和家長去的版本，就是只能瀏覽但不能顯示答案或者專門為學習者設計，就可以完美解決這些問題。

##如何使用
以下指令碼託管於儲存庫[ without -auth_e-book/fast.js ] ( https://github.com/notlin4/without-auth_e-book/blob/main/fast.js )，並使用[ jsDelivr ] ( https://www.jsdelivr.com/ ) 快取資源，更新日誌可於[這裡] (jsdelivr.com/ )快取資源，更新日誌可在[這裡] https://github.com/notlin4/without-auth_e-book/commits/main/fast.js ）查看。  
以下指令碼託管於儲存庫[ without -auth_e-book/fast.js ] ( https://github.com/notlin4/without-auth_e-book/blob/main/fast.js )，並使用[ jsDelivr ] ( https://www.jsdelivr.com/ ) 快取資料，更新日誌可在[這裡] (jsdelivr.com/ )快取資料，更新日誌可在[這裡] https://github.com/notlin4/without-auth_e-book/commits/main/fast.js ）查看。  
**請勿更改以下所有帳號的個人資料！**

###支援網站：
@@ -32,7 +32,7 @@ javascript:(function(){var script=document.createElement('script');script.src='h
4 .前往要使用的電子書或相關工具網站，點選書籤或在網址列輸入書籤的名稱。
5 .達成交付登錄！

如要在手機或平板電腦上使用，請輕觸「檢視方式」並遵循以下步驟操作：
如要在手機或平板電腦上使用，請輕觸「檢視方式」並遵循以下步驟操作：
<詳細資料>
    <summary>檢視方法</summary>

@@ -60,9 +60,9 @@ javascript:(function(){var script=document.createElement('script');script.src='h

如果您使用的是繁體中文（如上圖），請輸入「`允許貼上`」，然後按 Enter 鍵。

![中文] ( https://gist.github.com/assets/121224522/11aa0d00-3684-4b16-b98a-7c0a6deff90b )
![中文] ( https://gist.github.com/assets/121224522/11aa0d00-3684-4b16-b98a-7c0a6deff90b )

如果您使用的是英文（如上圖），請輸入「`允許貼上`」，然後按 Enter 鍵。
如果您使用的是英文（如上圖），請輸入「`允許貼上`」，然後按 Enter 鍵。

其他語言，請輸入對應中的內容，然後按 Enter 鍵。
</詳情>
@@ -87,9 +87,9 @@ javascript:(function(){var script=document.createElement('script');script.src='h

如果您使用的是繁體中文（如上圖），請輸入「`允許貼上`」，然後按 Enter 鍵。

![中文] ( https://gist.github.com/assets/121224522/11aa0d00-3684-4b16-b98a-7c0a6deff90b )
![中文] ( https://gist.github.com/assets/121224522/11aa0d00-3684-4b16-b98a-7c0a6deff90b )

如果您使用的是英文（如上圖），請輸入「`允許貼上`」，然後按 Enter 鍵。
如果您使用的是英文（如上圖），請輸入「`允許貼上`」，然後按 Enter 鍵。

其他語言，請輸入對應的內容，然後按 Enter 鍵。
</詳情>
@@ -98,7 +98,7 @@ javascript:(function(){var script=document.createElement('script');script.src='h

### ✅ 康軒電子書與網頁媒體盒
連結：[國小領域] ( https://webetextbook.knsh.com.tw/2/index.html?code_ Degree=1 )｜[國小英文] ( https://webetextbook.knsh.com.tw/2/index.html?code_ Degree =3 )｜[國中領域＜)｜[國中輔材] ( https://digitalmaster.knsh.com.tw/ebook/review/ )｜[網頁媒體盒] ( https://digitalmaster.knsh.com.tw/downloader/box-web/index.html )  
**注意事項**：需要先點選要下載的電子書資源，再執行指令碼才會生效，且切換電子書資源需要再執行一次。目前電子書尚未支援一到五年級內容，目前可透過網頁媒體盒下載造成不便之處，各位見諒。
**注意事項**：需要先點選要下載的電子書，再執行指令碼才會生效，且每次切換電子書都需要再執行一次。目前電子書尚未支援一到五年級的內容，可改用網頁媒體盒進行下載。造成不便之處，小見諒解。
``` js
if ( window.location.href.startsWith ( “ https://webetextbook.knsh.com.tw/ ” ) ) {
  var執行=  false ;
@@ -107,7 +107,7 @@ if (window.location.href.startsWith("https://webetextbook.knsh.com.tw/")) {
      alert ( '請先點選你要使用的電子書再執行指令碼。' );
      已執行= 真；
    } else  if ( ! executed &&  button .getAttribute ( ' d - title ' ) .includes ( " (網頁版) " )) {
      alert ( '偵測到一到五年級的內容，目前不支持繞過一到五年級的電子書。造成不便，小見諒解。' );
      alert ( '偵測到一到五年級的內容，目前不支持繞過一到五年級的電子書，請改用網頁媒體盒進行下載。造成不便之處，我們見諒。' );
      已執行= 真；
    } else  if（！執行）{
      var link =  document.createElement ( ' a ' ) ;
@@ -138,7 +138,7 @@ if (window.location.href.startsWith("https://webetextbook.knsh.com.tw/")) {
if ( window.location.href.startsWith ( “ https://edisc3.hle.com.tw/edisc_v3 ” ) ) {
  讓時間= 新的 Date（）。getTime（）。toString（）;
  本地儲存。setItem ( “ last_signinX_v2023 ” ,時間); //將帳號登錄日期設定為目前時間，避免被取代為過渡
  本地儲存。setItem ( " roleX_v2023 " , "老師" ); // 將身分設定為老師
  本地儲存。setItem ( " roleX_v2023 " , "老師" ); // 將身分設為老師
  本地儲存。setItem ( " emailX_v2023 " , " test@test.com " ); //由於翰林電子書會驗證是否有設定郵件，只要設定即可使用
  localStorage。 O0cOsie3P40svSZXhhpNkvt-uZpdkZctVI4rl_SCYdBzniZjf25QaBRUIo0C9EHbHWOdk7G3hQ-gvwndFiz7ukku3r7pLJ97V_F-pqMWgvIgv IDrTPK0SRTYxTozhDTUXdJ20VsFQMOFbm466f2a0i6QJ4PXEjFak-qAZabOvrtG1Nuygc23xsMiDPjKdT9CnAy-biMyb-bN8CiIVECqpbFBk 45ap-1Ke_5e4pHA958vAbC9ti1aqzMCNqMyy3KwGaMitRlRM_kJ9krTB587_5ewd0GFFaiqX2jwaKZBGVJnBosrMU38d6Edue9puwMLm4TdgX2jwaKZBGVJnBosrMU38d6Edue9puwMLm4TdgX2jwaKZBGVJnBosrMU38d6Edue9puwMLm4TdgX2jwaKZBGVJnBosrMU38d6Edue9puwMLm4Tdg”）； // 設定驗證用的權限
  地點。重新載入（）；//重新載入網頁
@@ -200,7 +200,7 @@ if (window.location.href.startsWith("https://testbank.hle.com.tw")) {
``` js
if ( window.location.href.startsWith ( “ https://reference.hle.com.tw ” ) ) {
  sessionStorage.setItem("accessToken", “eyJhbGciOiJSUzI1NiIsImtpZCI6Ijg1NzgwNWYxZGQ3ZmE5YTZiNTI3ZjQ0ZWNmZmJkNDhjIiwidHlwIjoiwidHw; PPq5wOhITi3TRddTqfWq-_yHWAPf0jw9EYNWE2LTT7lkTBET-RO6dXSOOR9E7eHeXlaxwPCGKErK0JJYY_WxvgxmuARub2YiAmS2zYsHoIpBCE5 yMFkjw2HKKFQ4nMf_pQj8bazx6aYEFGRYL8K1vC8Y2omugd3igVbqF6IE7wjBg35CLiLt20aYpVYaNE8mikoCQjQ3BMIuuf_h0e61N5ZqqRUN lbJj-kjILJ2UjQ8x_5woE5ZB0kh6CJO-34ygGHcd7G17XUbuJY_Y-vuldpqexlo43SUDVmgkDiF1HkJuoEGQtzbV6auhqSHpRapN6ktJw7kw"); // 設置權杖
  會話存儲。setItem ( " userRole " , "老師" ); // 將身分設定為老師
  會話存儲。setItem ( " userRole " , "老師" ); // 將身分設為老師
  地點。重新載入（）；//重新載入網頁
} else  if ( window .confirm ( "網站錯誤，按一下「確定」來開啟翰林輔材網。 " )) {
  window.open ( ' https : //reference.hle.com.tw','_blank ' ) ;
@@ -211,7 +211,7 @@ if (window.location.href.startsWith("https://reference.hle.com.tw")) {
連結：[翰林教學資源] ( https://www.hle.com.tw/ )
``` js
if ( window.location.href.startsWith ( “ https://www.hle.com.tw ” ) ) {
  本地儲存。setItem ( "角色" , "老師" ); // 將身分設定為老師
  本地儲存。setItem ( "角色" , "老師" ); // 將身分設為老師
  localStorage.setItem("令牌", “eyJhbGciOiJSUzI1NiIsImtpZCI6Ijg1NzgwNWYxZGQ3ZmE5YTZiNTI3ZjQ0ZWNmZmJkNDhjIiwidHlwIjoiwidHlwIjoi_pmg00Q 2JXixdy2GFjKIREMBZqXWgu6uAsqk-HsAV_Hl8hW5OSH0lGZ9Gp4csGJcmN-JYip-8T0ZQG22QhXgsHc3wjCd-LJ7Z00w8DNmiQG22QhXgsHc3wjCd-LJ7Z00w8DNmimiQG22QhXgsHc3wjCd-LJ7Z00w8DNmimiwww. MVKTNSsDO2I9gCZAd0BOPYpCNFXzY6TTwH6V2hKW6XJ2RvO2uq-UmeSe-lpXVFaRJ5zohoP2bnn29HSJIwDh-wyroBVIz_2uEorj2Zi8PPcBb4A Ie4Co8X3F1sQYNMzNnxjlKLpfuQpBxt3bzIPAd9XFP6h_21pzVfB4bd6JSQNX3KJ8y0t0KWzWyIBhKf7UuB69q7RXzpgg2BXVclpzpg2BXGlp7
  地點。重新載入（）；//重新載入網頁
} else  if ( window .confirm ( "網站錯誤，按「確定」來開啟網站。" )) {
@@ -230,7 +230,7 @@ if (window.location.href.startsWith("https://www.hle.com.tw")) {
-密碼：` a1b2c3d4 `

**南一**
-帳號：`未經授權`
-頭像：` Saddled7129`
-密碼：` a1b2c3d4 `

##常見問題
@@ -266,7 +266,7 @@ if (window.location.href.startsWith("https://www.hle.com.tw")) {
>由於大部分的電子書是在開啟電子書時驗證身分，直接開啟電子書的網址即可繞過驗證（可將網址儲存到書籤）；本指令碼隨時都有可能失效，請在可用時請盡快下載所需的文件。
5 .我找到了新的方法或帳號，要怎麼提供給你？
>您可以透過Discord` @ notlin4`或電子郵件iamnotlin4+gist@gmail.com來聯絡，謝謝您！ 
>您可以使用Discord帳號` @notlin4`或電子郵件iamnotlin4+gist@gmail.com 來聯繫我，謝謝您！（請不要使用電子郵件或Discord傳送發生問題等訊息）。
</詳情>
##鳴謝
@notlin4 notlin4 修改了 這個要點2024年3月24日。
 修改了 1 個文件 ，其中 新增 1 項 ， 刪除 1 項。
 2 處修改：1 處新增 & 1 處刪除2 
without-auth_e-book_tutorial_免登錄電子書教學.md
原始文件行號	不同行號	差異線變化
@@ -23,7 +23,7 @@
-  **何嘉仁**：[何嘉仁電子書櫃] ( https://bookonline.hess.com.tw/bookcase/#/ )

###書籤版
1 .如果尚未開啟書籤列請用` Ctrl + B`開啟，然後對書籤列按滑鼠右鍵，選擇「新增網頁...」。
1 .如果尚未開啟書籤列請以` Ctrl + Shift + B `開啟，然後對書籤列按滑鼠右鍵，選擇「新增網頁...」。
2 .將名稱改為您想要使用的新名稱。
3 .將網址改成以下指令碼：
``` javascript
@notlin4 notlin4 修改了 這個要點2024年3月21日。
 修改了 1 個文件 ，其中 新增 3 項 ， 刪除 3 項。
 6 處修改：3 處新增 & 3 處刪除6 
without-auth_e-book_tutorial_免登錄電子書教學.md
原始文件行號	不同行號	差異線變化
@@ -153,7 +153,7 @@ if (window.location.href.startsWith("https://edisc3.hle.com.tw/edisc_v3")) {
if ( window.location.href.includes ( “ oneclass.com.tw ” ) ) {
  讓mockToken =  JSON.stringify ( {
  “代碼”： “成功”，
  jwt： eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJpc3MiOiJodHRwOi8vbXlhY2NvdW50Lm5hbmkuY29vbC8iLCJzdWIiOiJ1c2Vycy9iJ1c wiZnJvbSI6Ik5hbmkiLCJ1c2VybmFtZSI6InJhbWF3MTkzNDAiLCJlbWFpbHZhbGlkIjp0sIVlLCJtb2JpbGV2YWxpZCI6ZmFsc2UsIVlLCJtb2JpbGV2YWxpZCI6ZmFsc2UsIVlLCJtbIjoIjoic XcxOTM0MEB3aWtmZWUuY29tIiwidWlkIjoiMGYxZDQ3ODAtYTk3Yy0xMWVlLWE5M2MtMjVlYjM1MGQ3YWNmIiwianRpIjoiNmJj0Iz​ ZjUyLTk0M2QtMzJmNDJkNmVjOTgyIiwiaWF0IjoxNzA5MzkwMzU1LCJleHAiOjE3MTQ1NzQzNTV9.JLmzjfEhH4ddpvnZESO6FSULoTbquCEM20 " });
  jwt ：eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJpc3MiOiJodHRwOi8vbXlhY2NvdW50Lm5hbmkuY29vbC8iLCJzdW IiOiJ1c2Vycy93aXRob3V0YXV0aCIsImZyb20iOiJOYW5pIiwidXNlcm5hbWUiOiJ3aXRob3V0YXV0aCIsImVtYWlsdm FsaWQiOnRydWUsIm1vYmlsZXZhbGlkIjpmYWxzZSwiZW1haWwiOiJiOWo3OWEyZ0BkdWNrLmNvbSIsInVpZCI6I ​jczOTAxNWIwLWU3OTUtMTFlZS05NGVkLWI5ZDJmNjk5NGQyZCIsImp0aSI6ImJkNTdlYzEzLTNiZDEtNDM5OS1hNTNlL TkyNzVhNDNkYzJlYyIsImlhdCI6MTcxMTAzNDAxMiwiZXhwIjoxNzE2MjE4MDEyfQ.bHi4mgrDaxlsODByZtdEWzUG17KPixEnlVoIzR2twVYY } ); 
  讓欄位名稱=  " nani_oneclass_login_token " ;
  var d =  new  Date ();
  d . setTime ( d.getTime () + ( 1 * 24 *  60 * 60 * 1000  ) ) ;      
@@ -219,7 +219,7 @@ if (window.location.href.startsWith("https://www.hle.com.tw")) {
}
```

>最後測試時間：2024/ 1/27
>最後測試時間：2024/ 3/21
</詳情>
##可用帳號
@@ -230,7 +230,7 @@ if (window.location.href.startsWith("https://www.hle.com.tw")) {
-密碼：` a1b2c3d4 `

**南一**
-帳號：` ramaw19340 `
-帳號：`未經授權`
-密碼：` a1b2c3d4 `

##常見問題
@notlin4 notlin4 修改了 這個要點2024年3月12日。
 修改了 1 個文件 ，新增 13 處 ， 刪除 13 處。
 26 處修改：13 處新增 & 13 處刪除二十六 
without-auth_e-book_tutorial_免登錄電子書教學.md
原始文件行號	不同行號	差異線變化
@@ -6,7 +6,7 @@
###將請勿將本指令碼作為抄襲答案、指向等惡意目的，使用本指令碼，請「自行承擔」一切後果與風險。

##簡介
本指令碼用於繞過台灣電子書與教學工具的前置驗證，達成所需教師帳號即可使用。
本指令碼用於繞過台灣電子書與教學工具的預設驗證即可，達成所需教師帳號使用。

##開發緣由
究竟是因為開發者忘記帶課本，但又想探究課本的資料，心血來潮研究看看電子書的驗證設計。  
@@ -19,7 +19,7 @@
###支援網站：
-  **康軒** : [國小領域] ( https://webetextbook.knsh.com.tw/2/index.html?code_ Degree=1 ) ｜[國小英語] ( https://webetextbook.knsh.com.tw/2/index.html?code_ Degree=3 ) ｜[國中領域https://webetextbook.knsh.com.tw/2/index.html?code_ Degree= 2 )｜[國中輔材] ( https://digitalmaster.knsh.com.tw/ebook/review/ ) ｜[網頁媒體盒] ( https://digitalmaster.kdownsh.com./web.kdownshbox .
-  **翰林** : [翰林行動大師] ( https://edisc3.hle.com.tw/edisc_v3/ebook_v2023.html )｜[翰林雲端命題大師] ( https://testbank.hle.com.tw )｜[翰林輔材網] ( https: //reference.hle.com.twence )｜[翰林輔材網] (h.com https://www.hle.com.tw/ )
-  **南一** : [ OneBook電子書] ( https://reader.oneclass.com.tw/bookshelf )｜[ OneBox網頁版] ( https://onebox2.oneclass.com.tw )｜[ OnePaper線上雲端出題] ( https://onepaper.oneclass.com.tw )
-  **南一** : [ NaniBook電子書] ( https://reader.oneclass.com.tw/bookshelf )｜[ NaniBox網頁版] ( https://onebox2.oneclass.com.tw )｜[ NaniPaper線上雲端出題] ( https://onepaper.oneclass.com.tw )
-  **何嘉仁**：[何嘉仁電子書櫃] ( https://bookonline.hess.com.tw/bookcase/#/ )

###書籤版
@@ -75,7 +75,7 @@ javascript:(function(){var script=document.createElement('script');script.src='h

###指令碼版本
<詳細資料>
    <summary>點此展開</summary>
    <summary>進一步展開</summary>

1 .前往要使用的電子書或相關工具網站。
2 .按F12開啟開發人員工具，然後切換到主控台（Console）分頁。
@@ -140,7 +140,7 @@ if (window.location.href.startsWith("https://edisc3.hle.com.tw/edisc_v3")) {
  本地儲存。setItem ( “ last_signinX_v2023 ” ,時間); //將帳號登錄日期設定為目前時間，避免被取代為過渡
  本地儲存。setItem ( " roleX_v2023 " , "老師" ); //將身分設定為老師
  本地儲存。setItem ( " emailX_v2023 " , " test@test.com " ); //由於翰林電子書會驗證是否有設定郵件，只要設定即可使用
  localStorage。 O0cOsie3P40svSZXhhpNkvt-uZpdkZctVI4rl_SCYdBzniZjf25QaBRUIo0C9EHbHWOdk7G3hQ-gvwndFiz7ukku3r7pLJ97V_F-pqMWgvIgv IDrTPK0SRTYxTozhDTUXdJ20VsFQMOFbm466f2a0i6QJ4PXEjFak-qAZabOvrtG1Nuygc23xsMiDPjKdT9CnAy-biMyb-bN8CiIVECqpbFBk 45ap-1Ke_5e4pHA958vAbC9ti1aqzMCNqMyy3KwGaMitRlRM_kJ9krTB587_5ewd0GFFaiqX2jwaKZBGVJnBosrMU38d6Edue9puwMLm4TdgX2jwaKZBGVJnBosrMU38d6Edue9puwMLm4TdgX2jwaKZBGVJnBosrMU38d6Edue9puwMLm4Tdg”）； // 設定身份驗證的令牌使用權
  localStorage。 O0cOsie3P40svSZXhhpNkvt-uZpdkZctVI4rl_SCYdBzniZjf25QaBRUIo0C9EHbHWOdk7G3hQ-gvwndFiz7ukku3r7pLJ97V_F-pqMWgvIgv IDrTPK0SRTYxTozhDTUXdJ20VsFQMOFbm466f2a0i6QJ4PXEjFak-qAZabOvrtG1Nuygc23xsMiDPjKdT9CnAy-biMyb-bN8CiIVECqpbFBk 45ap-1Ke_5e4pHA958vAbC9ti1aqzMCNqMyy3KwGaMitRlRM_kJ9krTB587_5ewd0GFFaiqX2jwaKZBGVJnBosrMU38d6Edue9puwMLm4TdgX2jwaKZBGVJnBosrMU38d6Edue9puwMLm4TdgX2jwaKZBGVJnBosrMU38d6Edue9puwMLm4TdgX2jwaKZBGVJnBosrMU38d6Edue9puwMLm4Tdg”）； // 設定驗證用的權限
  地點。重新載入（）；//重新載入網頁
} else  if ( window .confirm ( "網站錯誤，按一下「確定」來開啟翰林行動大師。" )) {
  window.open ( ' https://edisc3.hle.com.tw/edisc_v3/ebook_v2023.html','_blank ' ) ;
@@ -164,7 +164,7 @@ if (window.location.href.includes("oneclass.com.tw")) {
  }別的{
    文件.cookie = fieldName + “ = ” + mockToken + “ ;  ” + expires + “ ; path =/ ” ;     
  }
  本地儲存。setItem ( “ nani_tokenInfo ” ,mockToken); // 設定身份驗證用的權杖
  本地儲存。setItem ( “ nani_tokenInfo ” ,mockToken); // 設定驗證用的權限
  地點。重新載入（）；//重新載入網頁
} else  if ( confirm ( '網站錯誤，請選擇要開啟的項目：\n\n 1.NaniBook電子書\n 2.NaniBox網頁版\n 3.NaniPaper線上雲端出題' )) {
  var selectedURL = [ ' https://reader.oneclass.com.tw/bookshelf ' , ' https://onebox2.oneclass.com.tw ' , ' https://onepaper.oneclass.com.tw ' ] [ parseInt ( Prompt ( '請輸入你的選擇（輸入數字 1、2 或 3) : ' ) ; 
@@ -212,7 +212,7 @@ if (window.location.href.startsWith("https://reference.hle.com.tw")) {
``` js
if ( window.location.href.startsWith ( “ https://www.hle.com.tw ” ) ) {
  本地儲存。setItem ( "角色" , "老師" ); //將身分設定為老師
  localStorage.setItem("令牌", “eyJhbGciOiJSUzI1NiIsImtpZCI6Ijg1NzgwNWYxZGQ3ZmE5YTZiNTI3ZjQ0ZWNmZmJkNDhjIiwidHlwIjoiwidHlwIjoi_pmg00Q 2JXixdy2GFjKIREMBZqXWgu6uAsqk-HsAV_Hl8hW5OSH0lGZ9Gp4csGJcmN-JYip-8T0ZQG22QhXgsHc3wjCd-LJ7Z00w8DNmiQG22QhXgsHc3wjCd-LJ7Z00w8DNmimiQG22QhXgsHc3wjCd-LJ7Z00w8DNmimiwww. MVKTNSsDO2I9gCZAd0BOPYpCNFXzY6TTwH6V2hKW6XJ2RvO2uq-UmeSe-lpXVFaRJ5zohoP2bnn29HSJIwDh-wyroBVIz_2uEorj2Zi8PPcBb4A Ie4Co8X3F1sQYNMzNnxjlKLpfuQpBxt3bzIPAd9XFP6h_21pzVfB4bd6JSQNX3KJ8y0t0KWzWyIBhKf7UuB69q7RXzpgg2BXGlp7mgx2BXGlp7mxB69q30m
  localStorage.setItem("令牌", “eyJhbGciOiJSUzI1NiIsImtpZCI6Ijg1NzgwNWYxZGQ3ZmE5YTZiNTI3ZjQ0ZWNmZmJkNDhjIiwidHlwIjoiwidHlwIjoi_pmg00Q 2JXixdy2GFjKIREMBZqXWgu6uAsqk-HsAV_Hl8hW5OSH0lGZ9Gp4csGJcmN-JYip-8T0ZQG22QhXgsHc3wjCd-LJ7Z00w8DNmiQG22QhXgsHc3wjCd-LJ7Z00w8DNmimiQG22QhXgsHc3wjCd-LJ7Z00w8DNmimiwww. MVKTNSsDO2I9gCZAd0BOPYpCNFXzY6TTwH6V2hKW6XJ2RvO2uq-UmeSe-lpXVFaRJ5zohoP2bnn29HSJIwDh-wyroBVIz_2uEorj2Zi8PPcBb4A Ie4Co8X3F1sQYNMzNnxjlKLpfuQpBxt3bzIPAd9XFP6h_21pzVfB4bd6JSQNX3KJ8y0t0KWzWyIBhKf7UuB69q7RXzpgg2BXVclpzpg2BXGlp7
  地點。重新載入（）；//重新載入網頁
} else  if ( window .confirm ( "網站錯誤，按「確定」來開啟網站。" )) {
  window.open ( ' https : //www.hle.com.tw','_blank ' ) ;
@@ -225,18 +225,18 @@ if (window.location.href.startsWith("https://www.hle.com.tw")) {
##可用帳號
**請勿更改以下所有帳號的個人資料！**

**南一**
-帳號：` ramaw19340 `
-密碼：` a1b2c3d4 `

**翰林**
-帳號：` ramaw19340@wikfee.com `
-密碼：` a1b2c3d4 `

**南一**
-帳號：` ramaw19340 `
-密碼：` a1b2c3d4 `

##常見問題
**你可以在留言區提問，但在提問前請先看這裡！**
<詳細資料>
    <summary>點此展開</summary>
    <summary>進一步展開</summary>

1 .為什麼具體的教學不見了？
>作者本教學為因果的分支（Fork）版本，原[菘菘] ( https://github.com/SiongSng )已刪除原教學，若要查看原因請點選下方「查看原因」來展開，也請各位不要討論版權法或出版商規範的話題。
@@ -263,7 +263,7 @@ if (window.location.href.startsWith("https://www.hle.com.tw")) {
>可以留言區詢問，我會試試看。由於龍騰的驗證機制破解，且無帳號參與測試，目前無法提供。
4.如何在開啟電子書時跳過驗證？
>由於大部分的電子書是在開啟電子書時驗證身體分，直接開啟電子書的網址即可繞過身體分驗證（可將網址儲存到書籤）；本指令碼隨時都有可能失效，請在可用時請盡快下載所需的文件。
>由於大部分的電子書是在開啟電子書時驗證身分，直接開啟電子書的網址即可繞過驗證（可將網址儲存到書籤）；本指令碼隨時都有可能失效，請在可用時請盡快下載所需的文件。
5 .我找到了新的方法或帳號，要怎麼提供給你？
>您可以透過Discord` @ notlin4`或電子郵件iamnotlin4+gist@gmail.com來聯絡，謝謝您！
@@ -279,7 +279,7 @@ if (window.location.href.startsWith("https://www.hle.com.tw")) {
如果你覺得這篇教學對你有幫助，請點選本篇教學最上方的星星圖標，支持我繼續製作下去！

##限制
- 因為本指令碼在少數網站上僅繞過了驗證的身體分數驗證，因此可能會導致無法使用儲存心率、監測記錄等功能。
- 因為本指令碼在少數網站上僅繞過了驗證，因此可能會導致無法使用儲存資料記錄、修改等功能。
-翰林版電子書每天會自動重設數據，因此需重新執行指令碼。
-翰林版電子書將於2024/6/30新增翰林帳號驗證，未來此破解方法可能無法使用，須尋找更好的解決方案。
-現有的一些指令碼有些地方的迴避方式不太好，將來也許可以用其他方式執行指令碼來交換編碼行為。
@notlin4 notlin4 修改了 這個要點2024年3月10日。
 修改了 1 個文件 ， 新增了 2 處 ， 刪除了 2 處。
 4 處修改：2 處新增 & 2 處刪除4 
without-auth_e-book_tutorial_免登錄電子書教學.md
原始文件行號	不同行號	差異線變化
@@ -189,7 +189,7 @@ if (!localStorage.getItem("isLogin")) {
連結：[翰林雲端命題大師] ( https://testbank.hle.com.tw )
``` js
if ( window.location.href.startsWith ( “ https://testbank.hle.com.tw ” ) ) {
  localStorage.setItem("oidc.user:https://id.hle.com.tw:js", '{“access_token”："eyJhbGciOiJSUzI1NiIsImtpZCI6Ijg1NzgwNWYxZGQ3ZmE5YTZiNTI3ZjQ0ZWNmZmJkNDhjIiwidHlwIjoiYXQQDIn0Ii ZXhhpNkvt-uZpdkZctVI4rl_SCYdBzniZjf25QaBRUIo0C9EHbHWOdk7G3hQ-gvwndFiz7 ukku3r7pLJ97V_F-pW9WgvIKhqMIDrTPK0SRTYxTozhDTUXdJ20VsFQMOFbm466f2a0i6QJ 4PXEjFak-qAZabOvrtG1Nuygc23xsMiDPjKdT9CnAy-biMyb-bN8CiIvCqpbFBkKOVE45ap-1Ke_5e4pHA958vAbC9ti1aqzMCNqqi3KwwMCN; waKZBGVJnBosrMU38d6Edue9puwMLm4Tdg","id_token":"eyJhbGciOiJSUzI1NiIsIm tpZCI6Ijg1NzgwNWYxZGQ3ZmE5YTZiNTI3ZjQ0ZMTI3ZfZoM2vdoz_l88dbNGaciNKvTWg81Bfu_Magpn7yEyTqYSKzBdiXbBS7dA5aoXflmI1WcKBfspDK5lQSZXtkvLV Uyw5ZXNdu4x3mhJ2_LFsGSIqR2KG1mhcwvOkbrs7srAR1fKRtELuKMDrOGwv401QxrZYgSVOTcr3Ael0IkZ3RZ9 woCslN4vHOOtjZ_7bnz5Khgb94tdJK7Yu7EkESOhZiNJRdn_3VqG3CYqwtgJzVxuXhKjrZhK8xDEYfhhcjpkBP2 Mlv7VB7a-ISzysHlaxHFfP3ie91D6wiOn-JPqxHtfAQbjFXmJN9xJyJnu5By1awl7iN3Yf3f7nv8huOiBw"}');
  localStorage.setItem("oidc.user:https://id.hle.com.tw:js", '{“access_token”：“eyJhbGciOiJSUzI1NiIsImtpZCI6Ijg1NzgwNWYxZGQ3ZmE5YTZiNTI3ZjQ0ZWNmZmJkNDhjIiwidHlwIjoiNTI3ZjQ0ZWNmZmJkNDhjIiwidHlwIjoiYXQQ5901ZFXQ59 OISwQo99RwPj0mTHnb9Aod2_hDKuzqvxSXO4sIcuzNesa8WcoAJUd3ZdIgsPlIpFGxuioN xEsbWbm-sR9tv-OQUdiEuAXSAkiB_-1y5TKeUbF_nDxQ-KjwjAiwkaLqyXA2cGcpX3j2F7v J5fU8rkEqmHyjMeoRV25Qc3cqSQfqmzTbZnLfJzS7tnM00zoIPrb9NPIKnMTm0LNipFd_u AzxCGQzsal0Gyxm5Hd45Hjk4GFu2fPtOtq2U4bBjKcaRljD8LwUhMFZH_PGkuOxncZHvS8h c-Lx9YS3QgQDuOELKc6UgRsMZ7008ql7uA","id_token":"eyJhbGciOiJSUzI1NiIsIm tpZCI6Ijg1NzgwNWYxZGQ3ZmE5YTZiNTI3ZjQ0ZWNmZmJkNDhjIiwidHlwIjoiSldUIn0..PK3xCNkOkgHw-peD_QwuWH7XlPJCiMCdX5QFh_clfh31km-Bl9uLxvEkqO4VSpGgP2ZUSyoU0Y1D-xzi44Rmjy lv0GJcuIViAyU_5UgyjpxJFtB0J8NDzegnIenr3QzJPOqItWA7y4BkMMp79gjNtBwU3kEuMliIYqgdaM_pEZB_G 8nnU_1moaI-drcHejk-p_GynCmJl2HMfquxwRR66d5g9QXdYm08x3491J6COdAKgMej7mNt6Z4GnMKMamIx7gJA Dre3Hd563qHWBxSmj9MGPkl9xEvKWAEMU_jg_A6KNQICUb-B0YfD3sh4IqLi5ZkPIGZV1EuKNUoxLE6Kpw”}');
  地點。重新載入（）；//重新載入網頁
} else  if ( window .confirm ( "網站錯誤，按「確定」來開啟網站。" )) {
  window.open ( ' https : //testbank.hle.com.tw','_blank ' ) ;
@@ -287,6 +287,6 @@ if (window.location.href.startsWith("https://www.hle.com.tw")) {
---

腳本由[ SiongSng ] ( https://github.com/SiongSng )製作，由[ notlin4 ] ( https://github.com/notlin4 )繼續| 本指令代碼由[菘菘]   ( https://github.com/SiongSng )製作，由[ notlin4 ] ( https://github.com/SiongSng )製作，由[ notlin4 ] ( https://notubub.com/not 4ub ) .
版權所有 © 2022-2024 [菘菘] ( https://github.com/SiongSng )和[ notlin4 ] ( https://github.com/notlin4 )。保留一切權利。  
版權所有 © 2022-2024 [菘菘] ( https://github.com/SiongSng )和[ notlin4 ] ( https://github.com/notlin4 )。版權所有，並一切保留權利。  
版權所有 © 2022-2024 [ SiongSng ] ( https://github.com/SiongSng )和[ notlin4 ] ( https://github.com/notlin4 )。保留所有權利。
![ ] ( https://hit.yhype.me/github/profile?user_id=121224522 ) <!--觀看次數追蹤 https://yhype.me/github/profile-views -->
@notlin4 notlin4 修改了 這個要點2024年3月6日。
 修改了 1 個文件 ， 新增了 2 處 ， 刪除了 2 處。
 4 處修改：2 處新增 & 2 處刪除4 
without-auth_e-book_tutorial_免登錄電子書教學.md
原始文件行號	不同行號	差異線變化
@@ -148,7 +148,7 @@ if (window.location.href.startsWith("https://edisc3.hle.com.tw/edisc_v3")) {
```

### ✅ 南一
連結：[ OneBook電子書] ( https://reader.oneclass.com.tw/bookshelf )｜[ OneBox網頁版] ( https://onebox2.oneclass.com.tw/ )｜[ OnePaper線上雲端出題] ( https://onepaper.oneclass.com.tw/ )
連結：[ NaniBook電子書] ( https://reader.oneclass.com.tw/bookshelf )｜[ NaniBox網頁版] ( https://onebox2.oneclass.com.tw/ )｜[ NaniPaper線上雲端出題] ( https://onepaper.oneclass.com.tw/ )
``` js
if ( window.location.href.includes ( “ oneclass.com.tw ” ) ) {
  讓mockToken =  JSON.stringify ( {
@@ -166,7 +166,7 @@ if (window.location.href.includes("oneclass.com.tw")) {
  }
  本地儲存。setItem ( “ nani_tokenInfo ” ,mockToken); //設定身份驗證用的權杖
  地點。重新載入（）；//重新載入網頁
} else  if ( confirm ( '網站錯誤，請選擇要開啟的項目：\n\n 1. OneBook電子書\n 2. OneBox網頁版\n 3. OnePaper線上雲端出題' )) {
} else  if ( confirm ( '網站錯誤，請選擇要開啟的項目：\n\n 1.NaniBook電子書\ n 2.NaniBox網頁版\n 3.NaniPaper線上雲端出題' ) ) {
  var selectedURL = [ ' https://reader.oneclass.com.tw/bookshelf ' , ' https://onebox2.oneclass.com.tw ' , ' https://onepaper.oneclass.com.tw ' ] [ parseInt ( Prompt ( '請輸入你的選擇（輸入數字 1、2 或 3) : ' ) ; 
  selectedURL &&  window.open ( selectedURL , ' _blank ' ) ;
}
@notlin4 notlin4 修改了 這個要點2024年3月6日。
 修改了 1 個文件 ， 新增了 2 處 ， 刪除了 2 處。
 4 處修改：2 處新增 & 2 處刪除4 
without-auth_e-book_tutorial_免登錄電子書教學.md
原始文件行號	不同行號	差異線變化
@@ -153,7 +153,7 @@ if (window.location.href.startsWith("https://edisc3.hle.com.tw/edisc_v3")) {
if ( window.location.href.includes ( “ oneclass.com.tw ” ) ) {
  讓mockToken =  JSON.stringify ( {
  “代碼”： “成功”，
  jwt： eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJpc3MiOiJodHRwOi8vbXlhY2NvdW50Lm5hbmkuY29vbC8iLCJzdWIiOiJ1c2Vycy9iJ1c wiZnJvbSI6Ik5hbmkiLCJ1c2VybmFtZSI6InJhbWF3MTkzNDAiLCJlbWFpbHZhbGlkIjp0sIVlLCJtb2JpbGV2YWxpZCI6ZmFsc2UsIVlLCJtb2JpbGV2YWxpZCI6ZmFsc2UsIVlLCJtbIjoIjoic XcxOTM0MEB3aWtmZWUuY29tIiwidWlkIjoiMGYxZDQ3ODAtYTk3Yy0xMWVlLWE5M2MtMjVlYjM1MGQ3YWNmIiwianRpIjoiNDBlMDY0jjoiND​ ZGUyLWFkM2UtZjA0ZDg2YjQwOGIxIiwiaWF0IjoxNzA0MjA2MTA4LCJleHAiOjE3MDkzOTAxMDh9.wHRXGTai3_3B9N2SlnQpSmDyOTAxMDh9.wHRXGTai3_3B9N2SlnQpSmDy_MW5p23. " });
  jwt： eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJpc3MiOiJodHRwOi8vbXlhY2NvdW50Lm5hbmkuY29vbC8iLCJzdWIiOiJ1c2Vycy9iJ1c wiZnJvbSI6Ik5hbmkiLCJ1c2VybmFtZSI6InJhbWF3MTkzNDAiLCJlbWFpbHZhbGlkIjp0sIVlLCJtb2JpbGV2YWxpZCI6ZmFsc2UsIVlLCJtb2JpbGV2YWxpZCI6ZmFsc2UsIVlLCJtbIjoIjoic XcxOTM0MEB3aWtmZWUuY29tIiwidWlkIjoiMGYxZDQ3ODAtYTk3Yy0xMWVlLWE5M2MtMjVlYjM1MGQ3YWNmIiwianRpIjoiNmJj0Iz​ ZjUyLTk0M2QtMzJmNDJkNmVjOTgyIiwiaWF0IjoxNzA5MzkwMzU1LCJleHAiOjE3MTQ1NzQzNTV9.JLmzjfEhH4ddpvnZESO6FSULoTbquCEM20 " });
  讓欄位名稱=  " nani_oneclass_login_token " ;
  var d =  new  Date ();
  d . setTime ( d.getTime () + ( 1 * 24 *  60 * 60 * 1000  ) ) ;      
@@ -281,7 +281,7 @@ if (window.location.href.startsWith("https://www.hle.com.tw")) {
##限制
-因為本指令碼在少數網站上僅繞過了驗證的身體分數驗證，因此可能會導致無法使用儲存心率、監測記錄等功能。
-翰林版電子書每天會自動重設數據，因此需重新執行指令碼。
-翰林版電子書將於2024/6/30新增翰林帳號驗證，未來此破解方法可能無法使用，需要尋找更好的解決方案。
-翰林版電子書將於2024/6/30新增翰林帳號驗證，未來此破解方法可能無法使用，須尋找更好的解決方案。
-現有的一些指令碼有些地方的迴避方式不太好，將來也許可以用其他方式執行指令碼來交換編碼行為。

---
@notlin4 notlin4 修改了 這個要點2024年2月22日。
 修改了 1 個文件 ，其中 新增 1 項 ， 刪除 1 項。
 2 處修改：1 處新增 & 1 處刪除2 
without-auth_e-book_tutorial_免登錄電子書教學.md
原始文件行號	不同行號	差異線變化
@@ -153,7 +153,7 @@ if (window.location.href.startsWith("https://edisc3.hle.com.tw/edisc_v3")) {
if ( window.location.href.includes ( “ oneclass.com.tw ” ) ) {
  讓mockToken =  JSON.stringify ( {
  “代碼”： “成功”，
  jwt ：eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJpc3MiOiJodHRwOi8vbXlhY2NvdW50Lm5hbmkuY29vbC8iLCJzdWIiOiJ1c2Vycy9MIsZM ImZyb20iOiJOYW5pIiwidXNlcm5hbWUiOiJMZW5zODM4MCIsImVtYWlsdmFsaWQiOnRydWUsIm1vYmlsZXZhbGlkIjpmYWxzZSwiZW1AwiZMi 3J4ZkBkdWNrLmNvbSIsInVpZCI6ImNhZWEzY2EwLTZlN2QtMTFlZS05NTlhLTJmNDEzZWZhMjIxZiIsImp0aSI6Ijc0NTJmNDEzZWZhMjIxZiIsImp0aSI6Ijc0NTRhY​ 1iZmJiLWIxZjEyNzE3MjFlYSIsImlhdCI6MTcwMjk4MzkzNywiZXhwIjoxNzA4MTY3OTM3fQ.HvQkN-h8Y0n5yFgQQ​​El3cM3fQ.HvQkN-h8Y0n5yFgQQ​​El3cM8XRMp1IEno50 " }); 
  jwt： eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJpc3MiOiJodHRwOi8vbXlhY2NvdW50Lm5hbmkuY29vbC8iLCJzdWIiOiJ1c2Vycy9iJ1c wiZnJvbSI6Ik5hbmkiLCJ1c2VybmFtZSI6InJhbWF3MTkzNDAiLCJlbWFpbHZhbGlkIjp0sIVlLCJtb2JpbGV2YWxpZCI6ZmFsc2UsIVlLCJtb2JpbGV2YWxpZCI6ZmFsc2UsIVlLCJtbIjoIjoic XcxOTM0MEB3aWtmZWUuY29tIiwidWlkIjoiMGYxZDQ3ODAtYTk3Yy0xMWVlLWE5M2MtMjVlYjM1MGQ3YWNmIiwianRpIjoiNDBlMDY0jjoiND​ ZGUyLWFkM2UtZjA0ZDg2YjQwOGIxIiwiaWF0IjoxNzA0MjA2MTA4LCJleHAiOjE3MDkzOTAxMDh9.wHRXGTai3_3B9N2SlnQpSmDyOTAxMDh9.wHRXGTai3_3B9N2SlnQpSmDy_MW5p23. " });
  讓欄位名稱=  " nani_oneclass_login_token " ;
  var d =  new  Date ();
  d . setTime ( d.getTime () + ( 1 * 24 *  60 * 60 * 1000  ) ) ;      
@notlin4 notlin4 修改了 這個要點2024年2月21日。
 修改了 1 個文件 ，新增 13 處 ， 刪除 2 處。
 15 處修改：13 處新增 & 2 處刪除15 
without-auth_e-book_tutorial_免登錄電子書教學.md
原始文件行號	不同行號	差異線變化
@@ -64,7 +64,7 @@ javascript:(function(){var script=document.createElement('script');script.src='h

如果您使用的是英文（如上圖），請輸入「`允許貼上`」，然後按 Enter 鍵。

其他語言，請輸入對應的內容，然後按 Enter 鍵。
其他語言，請輸入對應中的內容，然後按 Enter 鍵。
</詳情>

4 .達成交付登錄！
@@ -222,6 +222,17 @@ if (window.location.href.startsWith("https://www.hle.com.tw")) {
>最後測試時間：2024/1/27
</詳情>
##可用帳號
**請勿更改以下所有帳號的個人資料！**

**南一**
-帳號：` ramaw19340 `
-密碼：` a1b2c3d4 `

**翰林**
-帳號：` ramaw19340@wikfee.com `
-密碼：` a1b2c3d4 `

##常見問題
**你可以在留言區提問，但在提問前請先看這裡！**
<詳細資料>
@@ -262,7 +273,7 @@ if (window.location.href.startsWith("https://www.hle.com.tw")) {
-感謝** [菘菘] ( https://github.com/SiongSng ) **製作了原始教學。 （[原教學] ( https://gist.github.com/SiongSng/baa4f015258d0312f627b5659d93d72e )已刪除，原始內容[文件] ( https://gist.github.com/tom Cheng1111/ 3c647b6b09 )於 2022/2/1），請參閱常見問題第 1 項）
-感謝** <ins> @foxvegajian </ins> **提供康軒網頁媒體盒的下載方法。 ( [原訊息] ( https://gist.github.com/aliyaliu368/891eef75e09494e965d291ead4a80d17?permalink_comment_id=4685986#gistcomment-4685986 ) ）
-感謝** <ins> @ J56tw </ins> **提供康軒電子書的免登入方法。( [原訊息] ( https://gist.github.com/notlin4/a05d7db77cd5606a812f4b9900fef3ee?permalink_comment_id=4788981#gistcomment-4788981 )）
-感謝** < ins > @ tmyrhs3 </ ins > ** 提供翰林的頭像。 （[原訊息] ( https://gist.github.com/notlin4/a05d7db77cd5606a812f4b9900fef3ee?permalink_comment_id=4814684#gistcomment-4814684 )）
-感謝** < ins > @ tmyrhs3 </ ins > ** 提供翰林與南一帳號。 （[原訊息] ( https://gist.github.com/notlin4/a05d7db77cd5606a812f4b9900fef3ee?permalink_comment_id=4814684#gistcomment-4814684 )）
-最後感謝所有回答別人問題的人！

如果你覺得這篇教學對你有幫助，請點選本篇教學最上方的星星圖標，支持我繼續製作下去！
@notlin4 notlin4 修改了 這個要點2024年1月27日。
 修改了 1 個文件 ，其中 新增 1 項 ， 刪除 1 項。
 2 處修改：1 處新增 & 1 處刪除2 
without-auth_e-book_tutorial_免登錄電子書教學.md
原始文件行號	不同行號	差異線變化
@@ -278,4 +278,4 @@ if (window.location.href.startsWith("https://www.hle.com.tw")) {
腳本由[ SiongSng ] ( https://github.com/SiongSng )製作，由[ notlin4 ] ( https://github.com/notlin4 )繼續| 本指令代碼由[菘菘]   ( https://github.com/SiongSng )製作，由[ notlin4 ] ( https://github.com/SiongSng )製作，由[ notlin4 ] ( https://notubub.com/not 4ub ) .
版權所有 © 2022-2024 [菘菘] ( https://github.com/SiongSng )和[ notlin4 ] ( https://github.com/notlin4 )。保留一切權利。  
版權所有 © 2022-2024 [ SiongSng ] ( https://github.com/SiongSng )和[ notlin4 ] ( https://github.com/notlin4 )。保留所有權利。
![ ] ( https://hit.y-hype.me/github/profile?user_id=121224522 ) <!--觀看次數追蹤https://yhype.me/github/profile-views -->
![ ] ( https://hit.yhype.me/github/profile?user_id=121224522 ) < !--觀看次數追蹤https://yhype.me/github/profile-views -->
@notlin4 notlin4 修改了 這個要點2024年1月27日。
 修改了 1 個文件 ，其中 新增 3 項 ， 刪除 3 項。
 6 處修改：3 處新增 & 3 處刪除6 
without-auth_e-book_tutorial_免登錄電子書教學.md
原始文件行號	不同行號	差異線變化
@@ -199,7 +199,7 @@ if (window.location.href.startsWith("https://testbank.hle.com.tw")) {
連結：[翰林輔材網] ( https://reference.hle.com.tw )
``` js
if ( window.location.href.startsWith ( “ https://reference.hle.com.tw ” ) ) {
  會話存儲。setItem ( “ userToken ” , “ mockToken ” ); //設定假的權杖
  sessionStorage.setItem("accessToken", “eyJhbGciOiJSUzI1NiIsImtpZCI6Ijg1NzgwNWYxZGQ3ZmE5YTZiNTI3ZjQ0ZWNmZmJkNDhjIiwidHlwIjoiwidHw; PPq5wOhITi3TRddTqfWq-_yHWAPf0jw9EYNWE2LTT7lkTBET-RO6dXSOOR9E7eHeXlaxwPCGKErK0JJYY_WxvgxmuARub2YiAmS2zYsHoIpBCE5 yMFkjw2HKKFQ4nMf_pQj8bazx6aYEFGRYL8K1vC8Y2omugd3igVbqF6IE7wjBg35CLiLt20aYpVYaNE8mikoCQjQ3BMIuuf_h0e61N5ZqqRUN lbJj-kjILJ2UjQ8x_5woE5ZB0kh6CJO-34ygGHcd7G17XUbuJY_Y-vuldpqexlo43SUDVmgkDiF1HkJuoEGQtzbV6auhqSHpRapN6ktJw7kw"); // 設置權杖
  會話存儲。setItem ( " userRole " , "老師" ); //將身分設定為老師
  地點。重新載入（）；//重新載入網頁
} else  if ( window .confirm ( "網站錯誤，按一下「確定」來開啟翰林輔材網。 " )) {
@@ -219,7 +219,7 @@ if (window.location.href.startsWith("https://www.hle.com.tw")) {
}
```

>最後測試時間：2024/1/16
>最後測試時間：2024/1/27
</詳情>
##常見問題
@@ -278,4 +278,4 @@ if (window.location.href.startsWith("https://www.hle.com.tw")) {
腳本由[ SiongSng ] ( https://github.com/SiongSng )製作，由[ notlin4 ] ( https://github.com/notlin4 )繼續| 本指令代碼由[菘菘]   ( https://github.com/SiongSng )製作，由[ notlin4 ] ( https://github.com/SiongSng )製作，由[ notlin4 ] ( https://notubub.com/not 4ub ) .
版權所有 © 2022-2024 [菘菘] ( https://github.com/SiongSng )和[ notlin4 ] ( https://github.com/notlin4 )。保留一切權利。  
版權所有 © 2022-2024 [ SiongSng ] ( https://github.com/SiongSng )和[ notlin4 ] ( https://github.com/notlin4 )。保留所有權利。
![ ] ( https://hit.yhype.me/github/profile?user_id=121224522 ) < !--觀看次數追蹤https://yhype.me/github/profile-views -->
![ ] ( https://hit.y-hype.me/github/profile?user_id=121224522 ) <!--觀看次數追蹤https://yhype.me/github/profile-views -->
@notlin4 notlin4 修改了 這個要點2024年1月16日。
 修改了 1 個文件 ，其中 新增 1 項 ， 刪除 1 項。
 2 處修改：1 處新增 & 1 處刪除2 
without-auth_e-book_tutorial_免登錄電子書教學.md
原始文件行號	不同行號	差異線變化
@@ -278,4 +278,4 @@ if (window.location.href.startsWith("https://www.hle.com.tw")) {
腳本由[ SiongSng ] ( https://github.com/SiongSng )製作，由[ notlin4 ] ( https://github.com/notlin4 )繼續| 本指令代碼由[菘菘]   ( https://github.com/SiongSng )製作，由[ notlin4 ] ( https://github.com/SiongSng )製作，由[ notlin4 ] ( https://notubub.com/not 4ub ) .
版權所有 © 2022-2024 [菘菘] ( https://github.com/SiongSng )和[ notlin4 ] ( https://github.com/notlin4 )。保留一切權利。  
版權所有 © 2022-2024 [ SiongSng ] ( https://github.com/SiongSng )和[ notlin4 ] ( https://github.com/notlin4 )。保留所有權利。
![ ] ( https://hit.y-hype.me/github/profile?user_id=121224522 ) <!--觀看次數追蹤https://yhype.me/github/profile-views -->
![ ] ( https://hit.yhype.me/github/profile?user_id=121224522 ) < !--觀看次數追蹤https://yhype.me/github/profile-views -->
@notlin4 notlin4 修改了 這個要點2024年1月16日。
 修改了 1 個文件， 新增 了 6 項內容 ， 刪除了 5 項內容。
 11 處修改：6 處添加，5 處刪除11 
without-auth_e-book_tutorial_免登錄電子書教學.md
原始文件行號	不同行號	差異線變化
@@ -76,6 +76,7 @@ javascript:(function(){var script=document.createElement('script');script.src='h
###指令碼版本
<詳細資料>
    <summary>點此展開</summary>

1 .前往要使用的電子書或相關工具網站。
2 .按F12開啟開發人員工具，然後切換到主控台（Console）分頁。
3 .貼上下方的指令碼並執行。
@@ -139,7 +140,7 @@ if (window.location.href.startsWith("https://edisc3.hle.com.tw/edisc_v3")) {
  本地儲存。setItem ( “ last_signinX_v2023 ” ,時間); //將帳號登錄日期設定為目前時間，避免被取代為過渡
  本地儲存。setItem ( " roleX_v2023 " , "老師" ); //將身分設定為老師
  本地儲存。setItem ( " emailX_v2023 " , " test@test.com " ); //由於翰林電子書會驗證是否有設定郵件，只要設定即可使用
  localStorage.setItem("tokenX_v2023", “eyJhbGciOiJSUzI1NiIsImtpZCI6Ijg1NzgwNWYxZGQ3ZmE5YTZiNTI3ZjQ0ZWNmZmJkNDhjIiwidHlwIlwIlwIlw; ULJHev9ButdBsX_lstI0sRX0D-XcOyvxkmagfipWGR5UkeT9DXV9aRAjH0VyXF1xR8ZcXyVwOfg9eSdl1vVR51CLv8pPmDaWFHDIjgIAoIevC9 IuukgcTkM34YdBgldEXoDopx4kpFxQvwtGHTbOkCm3maz6GQaxHHygNVAtlgP9MLZND1fdazsSikxpVNZL261Ib3tucd9zw1gs6aKOjKyJrnzEh JbYbcJcpuFrGLLrxCM-c4sxHvjSKgcZ0J3-nM-jL5l-ZSbLoVcufe808yOBr2UTjFHgWU_FMc2vK0zqcT7J_FbXURsoTpDBhos_MpO-OLg");
  localStorage。 O0cOsie3P40svSZXhhpNkvt-uZpdkZctVI4rl_SCYdBzniZjf25QaBRUIo0C9EHbHWOdk7G3hQ-gvwndFiz7ukku3r7pLJ97V_F-pqMWgvIgv IDrTPK0SRTYxTozhDTUXdJ20VsFQMOFbm466f2a0i6QJ4PXEjFak-qAZabOvrtG1Nuygc23xsMiDPjKdT9CnAy-biMyb-bN8CiIVECqpbFBk 45ap-1Ke_5e4pHA958vAbC9ti1aqzMCNqMyy3KwGaMitRlRM_kJ9krTB587_5ewd0GFFaiqX2jwaKZBGVJnBosrMU38d6Edue9puwMLm4TdgX2jwaKZBGVJnBosrMU38d6Edue9puwMLm4TdgX2jwaKZBGVJnBosrMU38d6Edue9puwMLm4Tdg”）； // 設定身份驗證的令牌使用權
  地點。重新載入（）；//重新載入網頁
} else  if ( window .confirm ( "網站錯誤，按一下「確定」來開啟翰林行動大師。" )) {
  window.open ( ' https://edisc3.hle.com.tw/edisc_v3/ebook_v2023.html','_blank ' ) ;
@@ -188,7 +189,7 @@ if (!localStorage.getItem("isLogin")) {
連結：[翰林雲端命題大師] ( https://testbank.hle.com.tw )
``` js
if ( window.location.href.startsWith ( “ https://testbank.hle.com.tw ” ) ) {
  localStorage.setItem("oidc.user:https://id.hle.com.tw:js", '{“access_token”：“eyJhbGciOiJSUzI1NiIsImtpZCI6Ijg1NzgwNWYxZGQ3ZmE5YTZiNTI3ZjQ0ZWNmZmJkNDhjIiwidHlwIjoiYXQrand0In0iYXQrand0In0 ..kUzuSlFgOLoDULJHev9ButdBsX_lstI0sRX0D-XcOyvxkmagfipWGR5UkeT9DXV9aRAjH0VyXF1xR8ZcXyVwOfg9eSdl1v51CLv8pVRPmDaWFHDI jgIAoI4evC9IuukgcTkM34YdBgldEXoDopx4kpFxQvwtGHTbOkCm3maz6GQaxHHygNVAtlgP9MLZND1fdazsSikxpVNZL261Ib3tucd9zw1gs6aKOjzw1gs6aKOjzw1gs6aKOjzw1gs6aKOjzw1gs6aKOjzw1gs6aKOjzw1gs6aKOjzw1gs6aKOjzw1gs6aKOjzw1gs6aKOjzw1 KyJrnzEhJbYbcJcpuFrGLLrxCM-c4sxHvjSKgcZ0J3-nM-jL5l-ZSbLoVcufe808yOBr2UTjFHgWU_FMc2vK0zqcT7J_FbXURURBr2UTjFHgWU_FMc2vK0zqcT7J_FbXURURBr2UTjFHgWU_FMc2vK0zqcT7J_FbXURURMpO-hos_LupOso Lg","id_token":"eyJhbGciOiJSUzI1NiIsImtpZCI6Ijg1NzgwNWYxZGQ3ZmE5YTZiNTI3ZjQ0ZWNmZmJkNDhjIiwidHlwIjoiNTI3ZjQ0ZWNmZmJkNDhjIiwidHlwIjoiSldUIn0..fZoMoM vdoz_l88dbNGaciNKvTWg81Bfu_Magpn7yEyTqYSKzBdiXbBS7dA5aoXflmI1WcKBfspDK5lQSZXtkvLVUyw5ZXNdu4x3mhJ2_LFsGSIqR2KG1mGSIqRw vOkbrs7srAR1fKRtELuKMDrOGwv401QxrZYgSVOtcr3Ael0IkZ3RZ9woCslN4vHOOtjZ_7bnz5Khgb94tdJK7Yu7EkESOhZiNJRdn_3VqG3CYg zVxuXhKjrZhK8xDEYfhhcjpkBP2Mlv7VB7a-ISzysHlaxHFfP3ie91D6wiOn-JPqxHtfAQbjFXmJN9xJyJnu5By1awl7iN3Yf3f7nv8huOiBw”');
  localStorage.setItem("oidc.user:https://id.hle.com.tw:js", '{“access_token”："eyJhbGciOiJSUzI1NiIsImtpZCI6Ijg1NzgwNWYxZGQ3ZmE5YTZiNTI3ZjQ0ZWNmZmJkNDhjIiwidHlwIjoiYXQQDIn0Ii ZXhhpNkvt-uZpdkZctVI4rl_SCYdBzniZjf25QaBRUIo0C9EHbHWOdk7G3hQ-gvwndFiz7 ukku3r7pLJ97V_F-pW9WgvIKhqMIDrTPK0SRTYxTozhDTUXdJ20VsFQMOFbm466f2a0i6QJ 4PXEjFak-qAZabOvrtG1Nuygc23xsMiDPjKdT9CnAy-biMyb-bN8CiIvCqpbFBkKOVE45ap-1Ke_5e4pHA958vAbC9ti1aqzMCNqqi3KwwMCN; waKZBGVJnBosrMU38d6Edue9puwMLm4Tdg","id_token":"eyJhbGciOiJSUzI1NiIsIm tpZCI6Ijg1NzgwNWYxZGQ3ZmE5YTZiNTI3ZjQ0ZMTI3ZfZoM2vdoz_l88dbNGaciNKvTWg81Bfu_Magpn7yEyTqYSKzBdiXbBS7dA5aoXflmI1WcKBfspDK5lQSZXtkvLV Uyw5ZXNdu4x3mhJ2_LFsGSIqR2KG1mhcwvOkbrs7srAR1fKRtELuKMDrOGwv401QxrZYgSVOTcr3Ael0IkZ3RZ9 woCslN4vHOOtjZ_7bnz5Khgb94tdJK7Yu7EkESOhZiNJRdn_3VqG3CYqwtgJzVxuXhKjrZhK8xDEYfhhcjpkBP2 Mlv7VB7a-ISzysHlaxHFfP3ie91D6wiOn-JPqxHtfAQbjFXmJN9xJyJnu5By1awl7iN3Yf3f7nv8huOiBw"}');
  地點。重新載入（）；//重新載入網頁
} else  if ( window .confirm ( "網站錯誤，按「確定」來開啟網站。" )) {
  window.open ( ' https : //testbank.hle.com.tw','_blank ' ) ;
@@ -218,7 +219,7 @@ if (window.location.href.startsWith("https://www.hle.com.tw")) {
}
```

>最後測試時間：2024/1/13
>最後測試時間：2024/1/16
</詳情>
##常見問題
@@ -254,7 +255,7 @@ if (window.location.href.startsWith("https://www.hle.com.tw")) {
>由於大部分的電子書是在開啟電子書時驗證身體分，直接開啟電子書的網址即可繞過身體分驗證（可將網址儲存到書籤）；本指令碼隨時都有可能失效，請在可用時請盡快下載所需的文件。
5 .我找到了新的方法或帳號，要怎麼提供給你？
>您可以透過電子郵件 iamnotlin4+gist@gmail.com來我的聯絡方式，謝謝您！
>您可以透過Discord` @ notlin4`或電子郵件iamnotlin4+gist@gmail.com來聯絡，謝謝您！ 
</詳情>
##鳴謝
@@ -277,4 +278,4 @@ if (window.location.href.startsWith("https://www.hle.com.tw")) {
腳本由[ SiongSng ] ( https://github.com/SiongSng )製作，由[ notlin4 ] ( https://github.com/notlin4 )繼續| 本指令代碼由[菘菘]   ( https://github.com/SiongSng )製作，由[ notlin4 ] ( https://github.com/SiongSng )製作，由[ notlin4 ] ( https://notubub.com/not 4ub ) .
版權所有 © 2022-2024 [菘菘] ( https://github.com/SiongSng )和[ notlin4 ] ( https://github.com/notlin4 )。保留一切權利。  
版權所有 © 2022-2024 [ SiongSng ] ( https://github.com/SiongSng )和[ notlin4 ] ( https://github.com/notlin4 )。保留所有權利。
![ ] ( https://hit.yhype.me/github/profile?user_id=121224522 ) < !--觀看次數追蹤https://yhype.me/github/profile-views -->
![ ] ( https://hit.y-hype.me/github/profile?user_id=121224522 ) <!--觀看次數追蹤https://yhype.me/github/profile-views -->
@notlin4 notlin4 修改了 這個要點2024年1月13日。
 修改了 1 個文件 ，其中 新增 1 項 ， 刪除 1 項。
 2 處修改：1 處新增 & 1 處刪除2 
without-auth_e-book_tutorial_免登錄電子書教學.md
原始文件行號	不同行號	差異線變化
@@ -218,7 +218,7 @@ if (window.location.href.startsWith("https://www.hle.com.tw")) {
}
```

>最後測試時間：2024/1/ 5
>最後測試時間：2024/1/13
</詳情>
##常見問題
@notlin4 notlin4 修改了 這個要點2024年1月13日。
 修改了 1 個文件 ，新增 7 項 ， 刪除 7 項。
 14 處修改：7 處添加，7 處刪除14 
without-auth_e-book_tutorial_免登錄電子書教學.md
原始文件行號	不同行號	差異線變化
@@ -1,6 +1,6 @@
#教學用電子書及相關工具免登教學

**使用本指令碼即代表您同意本[免責聲明] ( #免責聲明)。** 
**使用本指令碼即代表您同意本[免責聲明] ( #免責聲明)。**

##免責聲明
###將請勿將本指令碼作為抄襲答案、指向等惡意目的，使用本指令碼，請「自行承擔」一切後果與風險。
@@ -13,7 +13,7 @@
開發這個並不是希望拿真正的抄答案，是希望讓需要用的人可以使用，也希望各家出版社能夠提供一個學生和家長去的版本，就是只能瀏覽但不能顯示答案或者專門為學習者設計，就可以完美解決這些問題。

##如何使用
以下指令碼託管於儲存庫[ without -auth_e-book/fast.js ] ( https://github.com/notlin4/without-auth_e-book/blob/main/fast.js )，並使用[ jsDelivr ] ( https://www.jsdelivr.com/ )快取資源，更新日誌可於[這裡] (jsdelivr.com/ ) 快取資源，更新日誌可在[這裡] https://github.com/notlin4/without-auth_e-book/commits/main/fast.js ）查看。
以下指令碼託管於儲存庫[ without -auth_e-book/fast.js ] ( https://github.com/notlin4/without-auth_e-book/blob/main/fast.js )，並使用[ jsDelivr ] ( https://www.jsdelivr.com/ )快取資源，更新日誌可於[這裡] (jsdelivr.com/ ) 快取資源，更新日誌可在[這裡] https://github.com/notlin4/without-auth_e-book/commits/main/fast.js ）查看。  
**請勿更改以下所有帳號的個人資料！**

###支援網站：
@@ -42,7 +42,7 @@ javascript:(function(){var script=document.createElement('script');script.src='h
``` javascript
javascript :( function ( ) { var script = document . createElement ( ' script ' ) ; script . src = ' https://cdn.jsdelivr.net/gh/notlin4/without-auth_e-book@main/fast.js '​​​​​
```
4 .前往要使用電子書的網站，在網頁列中輸入書籤的名稱，輕觸它。
4 .前往要使用電子書的網站，在網頁列中輸入書籤的名稱並輕觸它。
5 .達成交付登錄！
</詳情>

@@ -97,7 +97,7 @@ javascript:(function(){var script=document.createElement('script');script.src='h

### ✅ 康軒電子書與網頁媒體盒
連結：[國小領域] ( https://webetextbook.knsh.com.tw/2/index.html?code_ Degree=1 )｜[國小英文] ( https://webetextbook.knsh.com.tw/2/index.html?code_ Degree =3 )｜[國中領域＜)｜[國中輔材] ( https://digitalmaster.knsh.com.tw/ebook/review/ )｜[網頁媒體盒] ( https://digitalmaster.knsh.com.tw/downloader/box-web/index.html )  
**注意事項**：需要先點選要下載的電子書資源，再執行指令碼才會生效，且切換電子書資源需要再執行一次。目前尚未支持網頁版，造成不便之處，小弟見諒。
**注意事項**：需要先點選要下載的電子書資源，再執行指令碼才會生效，且切換電子書資源需要再執行一次。目前電子書尚未支援一到五年級內容，目前可透過網頁媒體盒下載造成不便之處，各位見諒。
``` js
if ( window.location.href.startsWith ( “ https://webetextbook.knsh.com.tw/ ” ) ) {
  var執行=  false ;
@@ -106,7 +106,7 @@ if (window.location.href.startsWith("https://webetextbook.knsh.com.tw/")) {
      alert ( '請先點選你要使用的電子書再執行指令碼。' );
      已執行= 真；
    } else  if ( ! executed &&  button .getAttribute ( ' d - title ' ) .includes ( " (網頁版) " )) {
      alert ( '偵測到網頁版內容，目前尚未支援此功能，造成不便之處，大家見諒。' );
      alert ( '偵測到一到五年級的內容，目前不支持繞過一到五年級的電子書。造成不便，小見諒解。' );
      已執行= 真；
    } else  if（！執行）{
      var link =  document.createElement ( ' a ' ) ;
@@ -257,7 +257,7 @@ if (window.location.href.startsWith("https://www.hle.com.tw")) {
>您可以透過電子郵件iamnotlin4+gist@gmail.com來我的聯絡方式，謝謝您！
</詳情>
##銘謝
##鳴謝@@ -20,6 +20,7 @@
-  **康軒** : [國中領域] ( https://webetextbook.knsh.com.tw/2/index.html?code_ Degree=2 )｜[國中輔材] ( https://digitalmaster.knsh.com.tw/ebook/review/ )
-  **翰林** : [翰林行動大師] ( https://edisc3.hle.com.tw/edisc_v3/ebook_v2023.html ) ｜ [翰林雲端命題大師] ( https://testbank.hle.com.tw )｜[翰林輔材網] (
-  **南一**：[ NaniBook 電子書] ( https://reader.oneclass.com.tw/bookshelf )｜[ NaniBox 網頁版] ( https://onebox2.oneclass.com.tw )｜[ NaniPaper 線上雲端出題] ( https://onepaper.twoneclass.com. tw)
-  **奇鼎事業**：[奇鼎數位書櫃] ( https://ebook02.chiding.com.tw/BookCase/publish/index.html )

###書籤版
1 .如果尚未開啟書籤列請以` Ctrl + Shift + B `開啟，然後對書籤列按滑鼠右鍵，選擇「新增網頁...」。
@@ -57,13 +58,13 @@ javascript:(function(){var script=document.createElement('script');script.src='h

![繁體中文] ( https://gist.github.com/assets/121224522/f1e71739-7a86-465b-bae5-965fcef6d23c )

如果你使用的是繁體中文（如上圖），請在控制台輸入「`允許貼上` ”，然後按 Enter 鍵允許貼上。
如果您使用的是繁體中文（如上圖），請在控制台輸入「`允許貼上` ”，然後按 Enter 鍵允許貼上。

![中文] ( https://gist.github.com/assets/121224522/11aa0d00-3684-4b16-b98a-7c0a6deff90b )

如果你使用的是中文（如上圖），請在控制台輸入「`允許貼上`」，並按 Enter 鍵允許貼上。
如果你使用的是中文（如上圖），請在主機控台輸入「`允許貼上`」，並按下Enter鍵允許貼上。

對於其他語言，請在控制台輸入對應中的內容，並按 Enter 鍵允許貼上。
其他語言，請在主控台輸入引號中的內容，並按 Enter 應答鍵允許貼上。
</詳情>

4 .達成交付登錄！
@@ -84,13 +85,13 @@ javascript:(function(){var script=document.createElement('script');script.src='h

![繁體中文] ( https://gist.github.com/assets/121224522/f1e71739-7a86-465b-bae5-965fcef6d23c )

如果你使用的是繁體中文（如上圖），請在控制台輸入「`允許貼上` ”，然後按 Enter 鍵允許貼上。
如果您使用的是繁體中文（如上圖），請在控制台輸入「`允許貼上` ”，然後按 Enter 鍵允許貼上。

![中文] ( https://gist.github.com/assets/121224522/11aa0d00-3684-4b16-b98a-7c0a6deff90b )

如果你使用的是中文（如上圖），請在控制台輸入「`允許貼上`」，並按 Enter 鍵允許貼上。
如果你使用的是中文（如上圖），請在主機控台輸入「`允許貼上`」，並按下Enter鍵允許貼上。

對於其他語言，請在控制台輸入對應中的內容，並按 Enter 鍵允許貼上。
其他語言，請在主控台輸入引號中的內容，並按 Enter 應答鍵允許貼上。
</詳情>

4 .達成交付登錄！
@@ -101,31 +102,51 @@ javascript:(function(){var script=document.createElement('script');script.src='h
**注意事項**：需要先點選要下載的電子書，再切換指令碼才會生效，且每次切換電子書都需要再執行一次。目前僅支援國中的電子書，國小電子書和媒體盒可暫時改用evonisme製作的[ EvGo ] ( https://github.com/evonisme/EvGo/tree/main )下載。造成不便，稍後見執行。
``` js
if ( window.location.href.startsWith ( “ https://webetextbook.knsh.com.tw/ ” ) ) {
  var執行=  false ;
  document.querySelectorAll ( ' .downAssetBtn ' ) .forEach ( function ( button ) {
    if ( ! executed && ( ! document.getElementById ( ' assetsPage ' ) || document.getElementById ( ' assetsPage ' ) . style.display === ' none ' ) ) {   
      alert ( '請先點選您要使用的電子書，再執行指令碼。' );
      已執行= 真；
    } else  if（！執行）{
      var link =  document.createElement ( ' a ' ) ;
      if ( window.location.href.startsWith ( “ https://webetextbook.knsh.com.tw/webcase/index.html ” ) ) {
        連結. href  =  ' https://storage1.knsh.com.tw/material/ '  + 按鈕. getAttribute ( ' d-file_name ' );
        關聯。textContent  =  '下載' ;
      } else  if ( window.location.href.startsWith ( “ https://webetextbook.knsh.com.tw/2/index.html ” ) ) { https://webetextbook.knsh.com.tw/2/index.html ” ) ) {
        link.href = ' https://webetextbook.knsh.com.tw/Ebookvieweran4Teacher/index.html?id= ' +（button.getAttribute ( ' d - file_name '  ) ? button.getAttribute ( ' d - file_name ' ) .replace ( ' button.getAttribute ( ' d - file_name ' ) .replace ( ' .    
        關聯。textContent  =  '開啟' ;
  const  assetButtons  =  document.querySelectorAll ( ' .downAssetBtn ' ) ;
  讓hasFileName =  false ;
  assetButtons.forEach (按鈕= > { 
    const  fileName  = 按鈕.getAttribute ( ' d - file_name ' );
    如果（檔名）{
      hasFileName =  true ;
      const  label  =  document.createElement ( ' a ' ) ;
      標籤. href  =  ` https://webetextbook.knsh.com.tw/Ebookvieweran4Teacher/index.html?id=${fileName . replace ( ' .zip ' , ' ' ) } ` ;
      標籤。textContent  =  '開啟' ;
      標籤.className = ' m- 0 標籤標籤資訊' ; 
      按鈕.innerHTML = ' ' ;    
      按鈕.appendChild (標籤) ;
      按鈕.removeAttribute ( ' onclick ' ) ;
    }
  });
  如果（hasFileName）{
    安慰。log ( '執行成功！' );
  }別的{
    alert ( '請先點選您要使用的電子書，再執行指令碼。' );
  }
} else  if ( window . location . href . startsWith ( ' https://digitalmaster.knsh.com.tw/v3/pages/j/index.html ' )) {
  讓alertShown =  false ;
  document.querySelectorAll ( ' . downloadButton ' ) . forEach ( button => { 
    const  urlMatch  =  button.getAttribute ( ' onclick ' ) ?. match ( / openeRefbook \( '( . * ? )' \ ) / ) ;
    如果（urlMatch ？ .[ 1 ]）{
      const  curBookUrl  =  new  URL (urlMatch[ 1 ]) . searchParams.get ( ' CUR_BOOK_URL ' ) ;
      如果（curBookUrl）{
        如果（！ alertShown）{
          警報（` CUR_BOOK_URL：${ curBookUrl } `）；
          alertShown =  true ;
          按鈕。textContent  =  "免登錄開啟" ;
          按鈕.removeAttribute ( ' onclick ' ) ;
          按鈕. addEventListener ( '點擊' , () => 視窗. open (urlMatch[ 1 ], ' _blank ' ));
        }
        返回;
      }
      按鈕.innerHTML = ' ' ;  
      按鈕.appendChild (連結)；
      本地儲存。setItem ( "登入帳號" , "模擬帳號" ); //設定假帳號
      本地儲存。setItem ( “ uuid ” , “ mockUUID ” ); //設定假UUID
}})} else  if ( window . location . href . startsWith ( ' https://digitalmaster.knsh.com.tw/downloader/box-web/index.html ' )) {
    }
  });
} else  if ( window . location . href . startsWith ( ' https://digitalmaster.knsh.com.tw/downloader/box-web/index.html ' )) {
  alert ( '請先選擇要使用的年級再執行指令碼。' );
} else  if ( window . location . href . startsWith ( ' https://digitalmaster.knsh.com.tw/ebook/review/ ' )) {
  alert ( '請先選擇要使用的電子書再執行指令碼。' );
} else  if ( confirm ( '網站錯誤，請選擇要開啟的項目：\n\n 1.國中領域\n 2.國中輔材' )) {
  var selectedURL = [ ' https://webetextbook.knsh.com.tw/2/index.html?code_ Degree=2 ' , ' https://digitalmaster.knsh.com.tw/ebook/review/ ' ][ parseInt ( prompt ( '請輸入你的選擇（輸入數字 1 或 2 )：1  ] ;
  selectedURL &&  window.open ( selectedURL , ' _blank ' ) ;
  const  selectedURL  = [ ' https://webetextbook.knsh.com.tw/2/index.html?code_ Degree=2 ' , ' https://digitalmaster.knsh.com.tw/ebook/review/ ' ][ parseInt ( Prompt ( '請輸入你的選擇（輸入數字 1 或 2 )：1  ] ;
  如果（selectedURL） 視窗.開啟（selectedURL，' _blank '）；
}
` ` `
@@ -151,7 +172,7 @@ if (window.location.href.startsWith("https://edisc3.hle.com.tw/edisc_v3")) {
if ( window.location.href.includes ( “ oneclass.com.tw ” ) ) {
  讓mockToken =  JSON.stringify ( {
  “代碼”： “成功”，
  jwt ：eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJpc3MiOiJodHRwOi8vbXlhY2NvdW50Lm5hbmkuY29vbC8iLCJzd WIiOiJ1c2Vycy91bmljeWNsZTQiLCJmcm9tIjoiTmFuaSIsInVzZXJuYW1lIjoidW5pY3ljbGU0IiwiZW1haWx2YWxp ZCI6dHJ1ZSwibW9iaWxldmFsaWQiOmZhbHNlLCJlbWFpbCI6ImtyNTJ5NTRtQGR1Y2suY29tIiwidWlkIjoiND​ A3YzBhNjAtMzgxZS0xMWVmLWEyZjMtMGYxNmE0Y2MyYjA4IiwianRpIjoiY2FjNDAzYjAtZjkyYS00YmY1LTg0MDktN WM1OTk1OGEwMTIxIiwiaWF0IjoxNzE5ODg4ODQzLCJleHAiOjE3MjUwNzI4NDN9.-usPxm8q72YvcAkqqdRSYoxVC-h2K862EV8DCtMZQCI “ ); 
  jwt ：eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJpc3MiOiJodHRwOi8vbXlhY2NvdW50Lm5hbmkuY29vbC8iLCJzd WIiOiJ1c2Vycy91bmljeWNsZTQiLCJmcm9tIjoiTmFuaSIsInVzZXJuYW1lIjoidW5pY3ljbGU0IiwiZW1haWx2YWxp ZCI6dHJ1ZSwibW9iaWxldmFsaWQiOmZhbHNlLCJlbWFpbCI6ImtyNTJ5NTRtQGR1Y2suY29tIiwidWlkIjoiND​ A3YzBhNjAtMzgxZS0xMWVmLWEyZjMtMGYxNmE0Y2MyYjA4IiwianRpIjoiMzEzNGE2ZDAtZTc0Zi00MDM0LTkzNjItM DY2YmI0NzA0YTcwIiwiaWF0IjoxNzI1MDczMzUyLCJleHAiOjE3MzAyNTczNTJ9.UIiK2nzCpv-F-LKYBWDEgsQQ5AdyW92tH5U9_t9Couo “ }); 
  讓欄位名稱=  " nani_oneclass_login_token " ;
  var d =  new  Date ();
  d . setTime ( d.getTime () + ( 1 * 24 *  60 * 60 * 1000  ) ) ;      
@@ -176,7 +197,7 @@ if (window.location.href.includes("oneclass.com.tw")) {
if ( window.location.href.startsWith ( “ https://testbank.hle.com.tw ” ) ) {
  localStorage.setItem("oidc.user:https://id.hle.com.tw:js", '{“access_token”：“eyJhbGciOiJSUzI1NiIsImtpZCI6Ijg1NzgwNWYxZGQ3ZmE5YTZiNTI3ZjQ0ZWNmZmJkNDhjIiwidHlwIjoiYXQQCInll-mZmJkJIiiwidHlwIjoiYXQQTInll CI6dHJ1ZSwibG9jayI6ZmFsc2UsInZlciI6Mywic2NvcGUIOlsib3BlbmlkIiwicHJvZm lsZSJdLCJhbXIiOlsicHdkIl19.d5gF0rVVmO_u28ZVVmO1 dQ0jjrqbyD0V0zlDpmDmnSBgJFoFVztO05cgQcwVzTwrFETG6c2t5zUESIUM0tEvvIlFNhGU1IQV6VNYxZJylghHCvwgONTBpjQUzbIxFnYIb4LNYxZJylghHCvwgONTBpjQUzbIxFnYIb4L144L1 uCwm2fF2gCao9Y9wl-BvruDtE5Oh0hyr7G8cBb0MefbBkd4aAwCUbxi1T-XQzTI​​XUPFl9TJq7ZQ6Rs-4gmj0edlsEv17sGFMFl9TJq7ZQ6Rs-4gmj0edlsEv17sGFMFl9TJq7ZQ6Rs-4gmj0edls wAixpYS7dwTKxRFDFXMxA","id_token":"eyJhbGciOiJSUzI1NiIsImtpZCI6Ijg1NzgwNWYxZGQ3ZmE5YTZiNTI3ZjQ0ZWNmZmJkNDhjIiwIHM​​ilwM​​iHlkNDhjIiw. WRlbnRpZmllZCI6dHJ1ZSwibG9jayI6ZmFsc2UsInZlciI6MywiYW1yIjpbInB3ZCJdfQ .v2vYQXQGgBDKgY6ggyy4V1Xv_K7aEz2vYQXGgBDKgY6g YCiD8qlNRb_D2Qp4AwC3q0L7j6l-qtEyrpzF7qI4LaWNw6N_MRKaP5m9-Zc9c6q1Q1miX yjFvjBJcwc3f2VdXEa5d49Qg9yHhdi3Y6RbQim8fuz-HR7MexEc94RGf0FS5Rc2EbixlEt kiYtziM9LfIRXskfy-wkUWdrHwwC7A_qQnuMiKIyUfQr0MEP9lH-lMZv6XtB0EapmfP4E wgTIK4Ak_dvzWQEffhyT36QbkmDkHYbQk1if9BcriXXgJgZ0Pz433_ETDgEHlULJg”}');
  地點。重新載入（）；//重新載入網頁
} else  if ( window .confirm ( "網站錯誤，按「確定」來開啟網站。" )) {
} else  if ( window .confirm ( "網站錯誤，按一下「確定」來開啟翰林雲端命題大師。" )) {
  window.open ( ' https : //testbank.hle.com.tw','_blank ' ) ;
}
` ` `
@@ -194,42 +215,42 @@ if (window.location.href.startsWith("https://reference.hle.com.tw")) {
` ` `
### ✅奇鼎事業
連結：[奇鼎事業] ( https://ebook02.chiding.com.tw/BookCase/publish/index.html )
連結：[奇鼎數位書櫃](https://ebook02.chiding.com.tw/BookCase/publish/index.html)
` ` ` js
if ( window.location.href.startsWith ( “ https://ebook02.chiding.com.tw/BookCase/publish/index.html ” ) ) {
    var執行=  false ;
    document.querySelectorAll ( ' .downAssetBtn ' ) .forEach ( function ( button ) {
      if ( ! executed && ( ! document.getElementById ( ' assetsPage ' ) || document.getElementById ( ' assetsPage ' ) . style.display === ' none ' ) ) {   
        alert ( '請先點選您要使用的電子書，再執行指令碼。' );
        已執行= 真；
      } else  if（！執行）{
        var link =  document.createElement ( ' a ' ) ;
          link.href = ' https://ebook02.chiding.com.tw/EbookViewer/publish/Ebook.html?id= ' + ( button.getAttribute ( ' d - file_name ' ) ? button.getAttribute ( ' d -  file_name ' ) .replace ( ' . ) ' , ' ) : '​​​    
          關聯。textContent  =  '開啟' ;
        按鈕.innerHTML = ' ' ;  
        按鈕.appendChild (連結)；
        本地儲存。setItem ( "登入帳號" , "模擬帳號" ); //設定假帳號
        本地儲存。setItem ( “ uuid ” , “ mockUUID ” ); //設定假UUID
  }})}
const  processedButtons  =  new  Set ();
函數 更新按鈕（）{
  if ( ! window.location.href.startsWith ( " https://ebook02.chiding.com.tw/ " ) ) {
    if ( window .confirm ( "網站錯誤，按「確定」來開啟奇鼎數位書櫃。" ) ) {
      window.open ( ' https://ebook02.chiding.com.tw/BookCase/publish/index.html','_blank ' ) ;
    }
    返回;
  }
  document.querySelectorAll ( ' .downAssetBtn ' ) .forEach (按鈕= > { 
    const  fileName  = 按鈕.getAttribute ( ' d - file_name ' );
    如果（檔案名稱&&  ！processedButtons。有（按鈕））{
      按鈕。內部 HTML  =  ' ' ; //清空按鈕內容
      按鈕。移除屬性( ' onclick ' ); //刪除舊的onclick事件
      const  label  =  document.createElement ( '標籤' ) ;
      標籤。textContent  =  '免登錄開啟' ;
      標籤.className = ' m- 0 標籤標籤資訊' ; 
      標籤.樣式.字體大小 =  '16 .5px ' ;
      label.onclick = ( ) = > window.open ( ` https://ebook02.chiding.com.tw/EbookViewer/publish/Ebook.html?id=$ { fileName.replace ( ' .zip ' , ' ' ) } ` , ' _ blank ' ) ;  
      按鈕。附加子（標籤）；//新增標籤
      處理過的按鈕。新增（按鈕）；//標記為已處理
      安慰。log ( `標籤已新增：${ fileName } ` );
    }
  });
}
新的 MutationObserver (updateButtons) .observe ( document.body，{childList : true  ， subtree :  true } );
更新按鈕(); //立即執行
` ` `
>最後測試時間：2024/9/22
>最後測試時間：2024/9/29
</詳情>
### ❌ 目前無效
<詳細資料>
    <summary>按這裡展開</summary>
### ❌康軒總複習即測卷
連結：[康軒總複習即測卷] ( https://ttrplatform.knsh.com.tw/teacher )
``` js
if ( window.location.href.startsWith ( “ https://ttrplatform.knsh.com.tw/ ” ) ) {
  文件. cookie = “ connect.sid=s%3AXM5bGeC2DRBIbxOybL3jxaUHrWUhone4.L298aSJXZtxyUyXBV6UTk4I5rYoWAJ0OYi1VyTfl% 2BXs ”  ； 
  視窗.位置.href = “ https://ttrplatform.knsh.com.tw/teacher ” ;  
} else  if ( window .confirm ( "網站錯誤，按一下「確定」來開啟翰林行動大師。" )) {
  window.open ( ' https://ttrplatform.knsh.com.tw/teacher','_blank ' ) ;
}
```

### ❌何嘉仁電子書
連結：[何嘉仁電子書櫃](https://bookonline.hess.com.tw/bookcase/#/)
` ` ` js
@notlin4 notlin4 修改了 這個要點2024年9月23日。
 修改了 1 個文件 ，其中 新增 1 項 ， 刪除 1 項。
 2 處修改：1 處新增 & 1 處刪除2 
without-auth_e-book_tutorial_免登錄電子書教學.md
原始文件行號	不同行號	差異線變化
@@ -296,7 +296,7 @@ if (!localStorage.getItem("isLogin")) {
-感謝** <ins> @foxvegajian </ins> **提供康軒網頁媒體盒的下載方法。 ( [原訊息] ( https://gist.github.com/aliyaliu368/891eef75e09494e965d291ead4a80d17?permalink_comment_id=4685986#gistcomment-4685986 ) ）
-感謝** <ins> @ J56tw </ins> **提供康軒電子書的免登入方法。( [原訊息] ( https://gist.github.com/notlin4/a05d7db77cd5606a812f4b9900fef3ee?permalink_comment_id=4788981#gistcomment-4788981 )）
-感謝** < ins > @ tmyrhs3 </ ins > **提供翰林帳號。 （[原訊息] ( https://gist.github.com/notlin4/a05d7db77cd5606a812f4b9900fef3ee?permalink_comment_id=4814684#gistcomment-4814684 )）
- 趕寫 ** <ins> @小哲<ins>提供奇鼎事業的免登入方法（Discord ）
- 感謝 ** <ins> @小哲<ins> **提供奇鼎事業的免登錄方法（Discord ）
-最後感謝所有回答別人問題的人！

如果你覺得這篇教學對你有幫助，請點選本篇教學最上方的星星圖標，支持我繼續製作下去！
@notlin4 notlin4 修改了 這個要點2024年9月22日。
 修改了 1 個文件 ，其中 新增 1 項 ， 刪除 5 項。
 6 處修改：1 處添加，5 處刪除6 
without-auth_e-book_tutorial_免登錄電子書教學.md
原始文件行號	不同行號	差異線變化
@@ -18,9 +18,8 @@

###支援網站
-  **康軒** : [國中領域] ( https://webetextbook.knsh.com.tw/2/index.html?code_ Degree=2 )｜[國中輔材] ( https://digitalmaster.knsh.com.tw/ebook/review/ )
-  **翰林** : [翰林行動大師] ( https://edisc3.hle.com.tw/edisc_v3/ebook_v2023.html )｜[翰林雲端命題大師] ( https://testbank.hle.com.tw )｜[翰林輔材網] ( https: //reference.hle.com.twence )｜[翰林輔材網] (h.com https://www.hle.com.tw/ )
-  **翰林** : [翰林行動大師] ( https://edisc3.hle.com.tw/edisc_v3/ebook_v2023.html ) ｜ [翰林雲端命題大師] ( https://testbank.hle.com.tw )｜[翰林輔材網] (
-  **南一**：[ NaniBook 電子書] ( https://reader.oneclass.com.tw/bookshelf )｜[ NaniBox 網頁版] ( https://onebox2.oneclass.com.tw )｜[ NaniPaper 線上雲端出題] ( https://onepaper.twoneclass.com. tw)
-  **何嘉仁**：[何嘉仁電子書櫃] ( https://bookonline.hess.com.tw/bookcase/#/ )

###書籤版
1 .如果尚未開啟書籤列請以` Ctrl + Shift + B `開啟，然後對書籤列按滑鼠右鍵，選擇「新增網頁...」。
@@ -107,9 +106,6 @@ if (window.location.href.startsWith("https://webetextbook.knsh.com.tw/")) {
    if ( ! executed && ( ! document.getElementById ( ' assetsPage ' ) || document.getElementById ( ' assetsPage ' ) . style.display === ' none ' ) ) {   
      alert ( '請先點選您要使用的電子書，再執行指令碼。' );
      已執行= 真；
    } else  if ( ! executed &&  button .getAttribute ( ' d - title ' ) .includes ( " (網頁版) " )) {
      alert ( '偵測到國小電子書，目前不支持繞過國小電子書，請暫時改用evonisme製作的EvGo下載。造成不便之處，我們見諒。' );
      已執行= 真；
    } else  if（！執行）{
      var link =  document.createElement ( ' a ' ) ;
      if ( window.location.href.startsWith ( “ https://webetextbook.knsh.com.tw/webcase/index.html ” ) ) {
@notlin4 notlin4 修改了 這個要點2024年9月22日。
 修改了 1 個文件 ，新增 62 項 ， 刪除 47 項。
 109 處修改：62 處添加，47 處刪除109 
without-auth_e-book_tutorial_免登錄電子書教學.md
原始文件行號	不同行號	差異線變化
@@ -16,8 +16,8 @@
以下指令碼託管於儲存庫[ without -auth_e-book/fast.js ] ( https://github.com/notlin4/without-auth_e-book/blob/main/fast.js )，並使用[ jsDelivr ] ( https://www.jsdelivr.com/ )快取資料，更新日誌可在[這裡] (jsdelivr.com/ )快取資料，更新日誌可在[這裡] https://github.com/notlin4/without-auth_e-book/commits/main/fast.js ）查看。  
**請勿更改以下所有帳號的個人資料！**

###支援網站：
-  **康軒** : [國小領域] ( https://webetextbook.knsh.com.tw/2/index.html?code_ Degree=1 ) ｜[國小英語] ( https://webetextbook.knsh.com.tw/2/index.html?code_ Degree=3 ) ｜[國中領域https://webetextbook.knsh.com.tw/2/index.html?code_ Degree= 2 )｜[國中輔材] ( https://digitalmaster.knsh.com.tw/ebook/review/ ) ｜[網頁媒體盒] ( https://digitalmaster.kdownsh.com./web.kdownshbox .
###支援網站
-  **康軒** : [國中領域] ( https://webetextbook.knsh.com.tw/2/index.html?code_ Degree=2 )｜[國中輔材] ( https://digitalmaster.knsh.com.tw/ebook/review/ )
-  **翰林** : [翰林行動大師] ( https://edisc3.hle.com.tw/edisc_v3/ebook_v2023.html )｜[翰林雲端命題大師] ( https://testbank.hle.com.tw )｜[翰林輔材網] ( https: //reference.hle.com.twence )｜[翰林輔材網] (h.com https://www.hle.com.tw/ )
-  **南一**：[ NaniBook 電子書] ( https://reader.oneclass.com.tw/bookshelf )｜[ NaniBox 網頁版] ( https://onebox2.oneclass.com.tw )｜[ NaniPaper 線上雲端出題] ( https://onepaper.twoneclass.com. tw)
-  **何嘉仁**：[何嘉仁電子書櫃] ( https://bookonline.hess.com.tw/bookcase/#/ )
@@ -96,9 +96,10 @@ javascript:(function(){var script=document.createElement('script');script.src='h

4 .達成交付登錄！

### ✅ 康軒電子書與網頁媒體盒
連結：[國小領域] ( https://webetextbook.knsh.com.tw/2/index.html?code_ Degree=1 )｜[國小英文] ( https://webetextbook.knsh.com.tw/2/index.html?code_ Degree =3 )｜[國中領域＜)｜[國中輔材] ( https://digitalmaster.knsh.com.tw/ebook/review/ )｜[網頁媒體盒] ( https://digitalmaster.knsh.com.tw/downloader/box-web/index.html )  
**注意事項**：需要先點選要下載的電子書，再執行指令碼才會生效，且每次切換電子書都需要再執行一次。目前電子書尚未支援一到五年級的內容，可改用網頁媒體盒進行下載。造成不便之處，小見諒解。

### ✅ 康軒電子書
連結：[國中領域] ( https://webetextbook.knsh.com.tw/2/index.html?code_ Degree=2 )｜[國中輔材] ( https://digitalmaster.knsh.com.tw/ebook/review/ )  
**注意事項**：需要先點選要下載的電子書，再切換指令碼才會生效，且每次切換電子書都需要再執行一次。目前僅支援國中的電子書，國小電子書和媒體盒可暫時改用evonisme製作的[ EvGo ] ( https://github.com/evonisme/EvGo/tree/main )下載。造成不便，稍後見執行。
``` js
if ( window.location.href.startsWith ( “ https://webetextbook.knsh.com.tw/ ” ) ) {
  var執行=  false ;
@@ -107,15 +108,15 @@ if (window.location.href.startsWith("https://webetextbook.knsh.com.tw/")) {
      alert ( '請先點選您要使用的電子書，再執行指令碼。' );
      已執行= 真；
    } else  if ( ! executed &&  button .getAttribute ( ' d - title ' ) .includes ( " (網頁版) " )) {
      alert ( '偵測到一到五年級的內容，目前不支持繞過一到五年級的電子書，請改用網頁媒體盒進行下載。造成不便之處，我們見諒。' );
      alert ( '偵測到國小電子書，目前不支持繞過國小電子書，請暫時改用evonisme製作的EvGo下載。造成不便之處，我們見諒。' );
      已執行= 真；
    } else  if（！執行）{
      var link =  document.createElement ( ' a ' ) ;
      if ( window.location.href.startsWith ( “ https://webetextbook.knsh.com.tw/webcase/index.html ” ) ) {
        連結. href  =  ' https://storage1.knsh.com.tw/material/ '  + 按鈕. getAttribute ( ' d-file_name ' );
        關聯。textContent  =  '下載' ;
      } else  if ( window.location.href.startsWith ( “ https://webetextbook.knsh.com.tw/2/index.html ” ) ) { https://webetextbook.knsh.com.tw/2/index.html ” ) ) {
        link . href  =  ' https://webetextbook.knsh.com.tw/  Ebookviewer4Teacher / Ebook .html ?id = ' +（ button . getAttribute ( ' d - file_name ' ) ?  button . getAttribute ( ' d - file_name ' ) . replace ( ' . 
        link . href  =  ' https://webetextbook.knsh.com.tw/ Ebookvieweran4Teacher/index  .html ?id= ' +（ button . getAttribute ( ' d -file_name ' ) ? button  .getAttribute ( ' d -file_name ' ) . replace ( ' button ' , ' .ipz ) ; 
        關聯。textContent  =  '開啟' ;
      }
      按鈕.innerHTML = ' ' ;  
@@ -126,23 +127,12 @@ if (window.location.href.startsWith("https://webetextbook.knsh.com.tw/")) {
  alert ( '請先選擇要使用的年級再執行指令碼。' );
} else  if ( window . location . href . startsWith ( ' https://digitalmaster.knsh.com.tw/ebook/review/ ' )) {
  alert ( '請先選擇要使用的電子書再執行指令碼。' );
} else  if ( confirm ( '網站錯誤，請選擇要開啟的項目：\n\n 1.國小領域\n 2.國小英語\n 3.國中領域\n 4.國中輔材\n 5.網頁媒體盒' )) {
  var selectedURL = [ ' https://webetextbook.knsh.com.tw/2/index.html?code_ Degree= 1 ' , ' https://webetextbook.knsh.com.tw/2/index.html?code_ Degree = 3 ' , ' https://webetextbook.tw/2/index.html?code_ Degree = 3 ' , ' https://webetextbook.M. digitalmaster.knsh.com.tw/ebook/review/ ' , ' https://digitalmaster.knsh.com.tw/downloader/box-web/index.html ' ][ parseInt ( prompt ( '請輸入你的選擇（輸入數字 1 、2、3、4或5 )：' ) - 11 ]; 
} else  if ( confirm ( '網站錯誤，請選擇要開啟的項目：\n\n 1.國中領域\n 2.國中輔材' )) {
  var selectedURL = [ ' https://webetextbook.knsh.com.tw/2/index.html?code_ Degree= 2 ' , ' https://digitalmaster.knsh.com.tw/ebook/review/ ' ] [ parseInt ( Prompt ( '請輸入你的選擇（輸入數字' 
  selectedURL &&  window.open ( selectedURL , ' _blank ' ) ;
}
```

### ✅康軒總複習即測卷
連結：[康軒總複習即測卷] ( https://ttrplatform.knsh.com.tw/teacher )
``` js
if ( window.location.href.startsWith ( “ https://ttrplatform.knsh.com.tw/ ” ) ) {
  文件. cookie = “ connect.sid=s%3AXM5bGeC2DRBIbxOybL3jxaUHrWUhone4.L298aSJXZtxyUyXBV6UTk4I5rYoWAJ0OYi1VyTfl% 2BXs ”  ； 
  視窗.位置.href = “ https://ttrplatform.knsh.com.tw/teacher ” ;  
} else  if ( window .confirm ( "網站錯誤，按一下「確定」來開啟翰林行動大師。" )) {
  window.open ( ' https://ttrplatform.knsh.com.tw/teacher','_blank ' ) ;
}
```

### ✅ 翰林電子書
連結：[翰林行動大師] ( https://edisc3.hle.com.tw/edisc_v3/ebook_v2023.html )  
``` js
@@ -151,7 +141,8 @@ if (window.location.href.startsWith("https://edisc3.hle.com.tw/edisc_v3")) {
  本地儲存。setItem ( “ last_signinX_v2023 ” ,時間); //將帳號登錄日期設定為目前時間，避免被取代為過渡
  本地儲存。setItem ( " roleX_v2023 " , "老師" ); //將身分設為老師
  本地儲存。setItem ( " emailX_v2023 " , " test@test.com " ); //由於翰林電子書會驗證是否有設定郵件，只要設定即可使用
  localStorage.setItem("tokenX_v2023", “eyJhbGciOiJSUzI1NiIsImtpZCI6Ijg1NzgwNWYxZGQ3ZmE5YTZiNTI3ZjQ0ZWNmZmJkNDhjjIiwidlw. 7YvKu2zsD4t8JoYLtUHeKopyBAb-mxneB3hU0Ejdt_-9iI-4z60_KEAnzLeBp2Gv0SSxpBgFdweRn31MIP4WHGCfpq4rPAGmdIpnWPUBTYywRcpnWPUB F7JOV_23qZIsyfXcj78K_FnBJwGuaT6J4oiyNSmuWjV7mx8tMj0IHINK3C5IJKmDDOX9ymmCk5WQ2mLuckjgel3uWoFxZTwT1mOxrVqGHmgYVo hrrt8f3YJuzLfoHxCmVQ6AW8zdc9OKi4xtaYwhHxjEOHZ5GFZ45uorWRxLIcuukdLLpUgQMl7awnL6yXbT-En7Bxzw-5v8P0WFhSI4tS8bHgSI4tS8bHg”；
  本地儲存。setItem ( “ lockX_v2023 ” , “假” );
  localStorage.setItem("tokenX_v2023", “eyJhbGciOiJSUzI1NiIsImtpZCI6Ijg1NzgwNWYxZGQ3ZmE5YTZiNTI3ZjQ0ZWNmZmJkNDhjIiwidH lwIjoiYXQrand0In0.-WwjyIsImlzaWRlbnRpZmllZCI6dHJ1ZSwibG9jayI6ZmFsc2UsInZlciI6Myw ic2NvcGUiOlsib3BlbmlkIiwicHJvZmlsZSIsImFwaTEiLCJJZGVudGl0eVNlcnZlckFwaSIsImhhbmx pbi1hcGkiLCJvZmZsaW5lX2FjY2VzcyJdLCJhbXIiOlsicHdkIl19.PGXhy1RBo_ff1lzvinDS8pR7qO eeotbQTaaW8kRRaF35Ga9QnhFM1FArfHXofPwNQvwok7KLfOosCA8iegJC2dN2EZPSflZMHD8VPn4UZ 6ZJTSAXt2s_T-hm6MEZM9iNoDerlam9G64evmtfrW0qygnLrMqVjGxVxXiy0pOM-8VcVMkc-iBNzZRV- vxnokS0jqQCTwAdkVMKCuFksrpRNtg2HLAAwVPosey5rjnBH4ivIMUey1dbZzaHRQwdZ3_ZDM5h9-j_1 LKGvrVpNQ-VcLc2-iShUVbb0bxwCzpkmTJ1ySSH4edZV36rFgXQNcDASARC5ujBUVQ79Brc6hR37w"); // 設定驗證用的權限
  地點。重新載入（）；//重新載入網頁
} else  if ( window .confirm ( "網站錯誤，按一下「確定」來開啟翰林行動大師。" )) {
  window.open ( ' https://edisc3.hle.com.tw/edisc_v3/ebook_v2023.html','_blank ' ) ;
@@ -183,24 +174,11 @@ if (window.location.href.includes("oneclass.com.tw")) {
}
```

### ✅ 何嘉仁電子書
連結：[何嘉仁電子書櫃] ( https://bookonline.hess.com.tw/bookcase/#/ )
``` js
if ( window.location.href.startsWith ( “ https://bookonline.hess.com.tw/bookcase/#/ ” ) ) {
if ( ! localStorage.getItem ( " isLogin " ) ) {
  本地儲存。setItem ( “ isLogin ” , “ true ” ); //將登入狀態設為true
  本地儲存。setItem ( " uuid " , " mock_user " ); //設定假的教師UUID
  地點。重新載入（）；//重新載入網頁
}} else  if ( window .confirm ( "網站錯誤，按一下「確定」來開啟何嘉仁電子書。" )) {
  window.open ( ' https://bookonline.hess.com.tw/bookcase/#/','_blank ' ) ;
}
```

### ✅ 翰林雲端命題大師
連結：[翰林雲端命題大師] ( https://testbank.hle.com.tw )
``` js
if ( window.location.href.startsWith ( “ https://testbank.hle.com.tw ” ) ) {
  localStorage.setItem("oidc.user:https://id.hle.com.tw:js", '{“access_token”：“eyJhbGciOiJSUzI1NiIsImtpZCI6Ijg1NzgwNWYxZGQ3ZmE5YTZiNTI3ZjQ0ZWNmZmJkNDhjIiwidHlwIjoiYXQrand0In0iYXQrand0In0 ..tRzJFMcjaxDj7YvKu2zsD4t8JoYLtUHeKopyBAb-mxneB3hU0Ejdt_-9iI-4z60_KEAnzLeBp2Gv0SSxpBgFdweRn31MIP4WHGCfpqLeBp2Gv0SSxpBgFdweRn31MIP4WHGCfpq4rPAGImd WPUBTYywRcXF7JOV_23qZIsyfXcj78K_FnBJwGuaT6J4oiyNSmuWjV7mx8tMj0IHINK3C5IJKmDDOX9ymmCk5WQ2mLuckjglel3uWoFxZTwT1mOx qGHmgYVohrrt8f3YJuzLfoHxCmVQ6AW8zdc9OKi4xtaYwhHxjEOHZ5GFZ45uorWRxLIcuukdLLpUgQMl7awnL6yXbT-En7Bxzw-5v8P0WFhSI4tS8b Hg","id_token":"eyJhbGciOiJSUzI1NiIsImtpZCI6Ijg1NzgwNWYxZGQ3ZmE5YTZiNTI3ZjQ0ZWNmZmJkNDhjIiwidHlwIjoiNTI3ZjQ0ZWNmZmJkNDhjIiwidHlwIjoiSldUIn0..cySod WB702wd4_IXGXWuwcas0m7jUL2VSCUnmHcTWKpNy7GPZTJv5FjMHVISwpViS8pxrWnKzd0YA3xCAopo7XB0_n1W8OjPb82dALd4nt-9xCAopo7XB0_n1W8OjPb82dALd4nt-9ozP0IedAOEo ji_2XoTf-TtBSCtsOFa6H6WZtRG4In8v-8fVLYrBVTdVs9mSiGAn_W7GQiI-fhbb6G3MM3ctKoPLg-0LmVELDbp0gFKNUbIQhpxIKS3M3ctIkpl3-f 2mT9OiGlgFieY6xhNpSyPCqnFA7HSvMHfJFYlgOfU2RdEJyZQSitbLYEsh-vNZrufrewpxW6Bdc4AqI4U_KXOrOoo1T7TowBWOg7dxLPHhw}'');
  localStorage.setItem("oidc.user:https://id.hle.com.tw:js", '{“access_token”：“eyJhbGciOiJSUzI1NiIsImtpZCI6Ijg1NzgwNWYxZGQ3ZmE5YTZiNTI3ZjQ0ZWNmZmJkNDhjIiwidHlwIjoiYXQQCInll-mZmJkJIiiwidHlwIjoiYXQQTInll CI6dHJ1ZSwibG9jayI6ZmFsc2UsInZlciI6Mywic2NvcGUIOlsib3BlbmlkIiwicHJvZm lsZSJdLCJhbXIiOlsicHdkIl19.d5gF0rVVmO_u28ZVVmO1 dQ0jjrqbyD0V0zlDpmDmnSBgJFoFVztO05cgQcwVzTwrFETG6c2t5zUESIUM0tEvvIlFNhGU1IQV6VNYxZJylghHCvwgONTBpjQUzbIxFnYIb4LNYxZJylghHCvwgONTBpjQUzbIxFnYIb4L144L1 uCwm2fF2gCao9Y9wl-BvruDtE5Oh0hyr7G8cBb0MefbBkd4aAwCUbxi1T-XQzTI​​XUPFl9TJq7ZQ6Rs-4gmj0edlsEv17sGFMFl9TJq7ZQ6Rs-4gmj0edlsEv17sGFMFl9TJq7ZQ6Rs-4gmj0edls wAixpYS7dwTKxRFDFXMxA","id_token":"eyJhbGciOiJSUzI1NiIsImtpZCI6Ijg1NzgwNWYxZGQ3ZmE5YTZiNTI3ZjQ0ZWNmZmJkNDhjIiwIHM​​ilwM​​iHlkNDhjIiw. WRlbnRpZmllZCI6dHJ1ZSwibG9jayI6ZmFsc2UsInZlciI6MywiYW1yIjpbInB3ZCJdfQ .v2vYQXQGgBDKgY6ggyy4V1Xv_K7aEz2vYQXGgBDKgY6g YCiD8qlNRb_D2Qp4AwC3q0L7j6l-qtEyrpzF7qI4LaWNw6N_MRKaP5m9-Zc9c6q1Q1miX yjFvjBJcwc3f2VdXEa5d49Qg9yHhdi3Y6RbQim8fuz-HR7MexEc94RGf0FS5Rc2EbixlEt kiYtziM9LfIRXskfy-wkUWdrHwwC7A_qQnuMiKIyUfQr0MEP9lH-lMZv6XtB0EapmfP4E wgTIK4Ak_dvzWQEffhyT36QbkmDkHYbQk1if9BcriXXgJgZ0Pz433_ETDgEHlULJg”}');
  地點。重新載入（）；//重新載入網頁
} else  if ( window .confirm ( "網站錯誤，按「確定」來開啟網站。" )) {
  window.open ( ' https : //testbank.hle.com.tw','_blank ' ) ;
@@ -210,27 +188,64 @@ if (window.location.href.startsWith("https://testbank.hle.com.tw")) {
連結：[翰林輔材網] ( https://reference.hle.com.tw )
``` js
if ( window.location.href.startsWith ( “ https://reference.hle.com.tw ” ) ) {
  sessionStorage.setItem("accessToken", “eyJhbGciOiJSUzI1NiIsImtpZCI6Ijg1NzgwNWYxZGQ3ZmE5YTZiNTI3ZjQ0ZWNmZmJkNDhjIiwFMHlwIjot 7YvKu2zsD4t8JoYLtUHeKopyBAb-mxneB3hU0Ejdt_-9iI-4z60_KEAnzLeBp2Gv0SSxpBgFdweRn31MIP4WHGCfpq4rPAGmdIpnWPUBTYywRcpnWPUB F7JOV_23qZIsyfXcj78K_FnBJwGuaT6J4oiyNSmuWjV7mx8tMj0IHINK3C5IJKmDDOX9ymmCk5WQ2mLuckjgel3uWoFxZTwT1mOxrVqGHmgYVo hrrt8f3YJuzLfoHxCmVQ6AW8zdc9OKi4xtaYwhHxjEOHZ5GFZ45uorWRxLIcuukdLLpUgQMl7awnL6yXbT-En7Bxzw-5v8P0WFhSI4tS8bHgSI4tS8bHg”）；
  sessionStorage.setItem("accessToken", “eyJhbGciOiJSUzI1NiIsImtpZCI6Ijg1NzgwNWYxZGQ3ZmE5YTZiNTI3ZjQ0ZWNmZmJkNDhj IiwidHlwIjoiYXQrand0In0.-WwjyIsImlzaWRlbnRpZmllZCI6dHJ1ZSwibG9jayI6ZmFsc2 UsInZlciI6Mywic2NvcGUiOlsib3BlbmlkIiwicHJvZmlsZSIsIm9mZmxpbmVfYWNjZXNzIl0 sImFtciI6WyJwd2QiXX0.xzaLXn13B5pOFPg7k7kOYcrHd3UGm2EIKaGJwHqcXY006ttgVygD O8MfcYMf3grrtgXPjbMZ_esLGu-hZqYb_Ajf_RfRfFtXexLeqeqewBaXWC1va-TrMuxjUCxrW_ByyO1gcNoTdyiuMSITR1TCepX3vEKC44N2ivWF4pDApDpDDpDpD進程進程44445444454pF44pDA4pDApDpkp 0UxfywQQAK_6lu9ifxqq359PvX_I1tnvLVP9hQKe8DfLujVAItPhaGJ-1luV5-UWJt8ooOuRc zYs1bqM5EMsV-iShCdVLvoTYYIaLRVy9dbEA84qRqvd0YE2Bmogat1STmNGRsryfNL66yEw"); // 設定權限
  sessionStorage.setItem("userToken", 「eyJhbGciOiJSUzI1NiIsImtpZCI6Ijg1NzgwNWYxZGQ3ZmE5YTZiNTI3ZjQ0ZWNmZmJkNDhjIiwidHlwIjoiSldUIn0.-WwjyIsImlWRmJjyIsImlJiS6ZmJZxjyIsIml 9jayI6ZmFsc2UsInZlciI6MywiYW1yIjpbInB3ZCJdfQ.TjqNUyWNAq7vhblmsAcAm8S5s-vk4_PuoczKvg1K8yv1W2XAwVWnzPJSvdh4158w -HNx0GVt4XqRn8EoKStyQF_66_i3jr5KsiUIQWlvCZAvm37akA74giYREgEBCG40c765lL0qqXFoVXaQ-Ko89_Qeu3GrfJcEI3yelZ7MRSP 4kMTqj_V0GSTSRTXleawGCQM7vQSgif7ylx5fwUT7O_Hg6mByuPDE9BRPBVweKqZdIzeSTGdjs8Hp87trAfL8RS_QMIJq_rExJc7byOYF9zN-e78_bzN-e // 設置權杖
  會話存儲。setItem ( " userRole " , "老師" ); //將身分設為老師
  地點。重新載入（）；//重新載入網頁
} else  if ( window .confirm ( "網站錯誤，按一下「確定」來開啟翰林輔材網。 " )) {
  window.open ( ' https : //reference.hle.com.tw','_blank ' ) ;
}
```

### ✅翰林教學資源
連結：[翰林教學資源] ( https:// www.hle .com.tw )
### ✅奇鼎事業
連結：[奇鼎事業] ( https:// ebook02.chiding .com.tw /BookCase/publish/index.html )
``` js
if ( window.location.href.startsWith ( “ https://www.hle.com.tw ” ) ) {
  本地儲存。setItem ( "角色" , "老師" ); //將身分設為老師
  localStorage.setItem("令牌", “eyJhbGciOiJSUzI1NiIsImtpZCI6Ijg1NzgwNWYxZGQ3ZmE5YTZiNTI3ZjQ0ZWNmZmJkNDhjIiwidHlFMwIjoiWrandjQ0ZWNmZmJkNDhjIiwidHlFMwIjoiY 7YvKu2zsD4t8JoYLtUHeKopyBAb-mxneB3hU0Ejdt_-9iI-4z60_KEAnzLeBp2Gv0SSxpBgFdweRn31MIP4WHGCfpq4rPAGmdIpnWPUBTYywRcpnWPUB F7JOV_23qZIsyfXcj78K_FnBJwGuaT6J4oiyNSmuWjV7mx8tMj0IHINK3C5IJKmDDOX9ymmCk5WQ2mLuckjgel3uWoFxZTwT1mOxrVqGHmgYVo hrrt8f3YJuzLfoHxCmVQ6AW8zdc9OKi4xtaYwhHxjEOHZ5GFZ45uorWRxLIcuukdLLpUgQMl7awnL6yXbT-En7Bxzw-5v8P0WFhSI4tS8bHgSI4tS8bHg”；
  地點。重新載入（）；//重新載入網頁
} else  if ( window .confirm ( "網站錯誤，按「確定」來開啟網站。" )) {
  window.open ( ' https : //www.hle.com.tw','_blank ' ) ;
if ( window.location.href.startsWith ( “ https://ebook02.chiding.com.tw/BookCase/publish/index.html ” ) ) {
    var執行=  false ;
    document.querySelectorAll ( ' .downAssetBtn ' ) .forEach ( function ( button ) {
      if ( ! executed && ( ! document.getElementById ( ' assetsPage ' ) || document.getElementById ( ' assetsPage ' ) . style.display === ' none ' ) ) {   
        alert ( '請先點選您要使用的電子書，再執行指令碼。' );
        已執行= 真；
      } else  if（！執行）{
        var link =  document.createElement ( ' a ' ) ;
          link.href = ' https://ebook02.chiding.com.tw/EbookViewer/publish/Ebook.html?id= ' + ( button.getAttribute ( ' d - file_name ' ) ? button.getAttribute ( ' d -  file_name ' ) .replace ( ' . ) ' , ' ) : '​​​    
          關聯。textContent  =  '開啟' ;
        按鈕.innerHTML = ' ' ;  
        按鈕.appendChild (連結)；
        本地儲存。setItem ( "登入帳號" , "模擬帳號" ); //設定假帳號
        本地儲存。setItem ( “ uuid ” , “ mockUUID ” ); //設定假UUID
  }})}
```
>最後測試時間：2024/9/22
</詳情>
### ❌ 目前無效
<詳細資料>
    <summary>按這裡展開</summary>

### ❌康軒總複習即測卷
連結：[康軒總複習即測卷] ( https://ttrplatform.knsh.com.tw/teacher )
``` js
if ( window.location.href.startsWith ( “ https://ttrplatform.knsh.com.tw/ ” ) ) {
  文件. cookie = “ connect.sid=s%3AXM5bGeC2DRBIbxOybL3jxaUHrWUhone4.L298aSJXZtxyUyXBV6UTk4I5rYoWAJ0OYi1VyTfl% 2BXs ”  ； 
  視窗.位置.href = “ https://ttrplatform.knsh.com.tw/teacher ” ;  
} else  if ( window .confirm ( "網站錯誤，按一下「確定」來開啟翰林行動大師。" )) {
  window.open ( ' https://ttrplatform.knsh.com.tw/teacher','_blank ' ) ;
}
```

>最後測試時間：2024/5/23
### ❌何嘉仁電子書
連結：[何嘉仁電子書櫃] ( https://bookonline.hess.com.tw/bookcase/#/ )
``` js
if ( window.location.href.startsWith ( “ https://bookonline.hess.com.tw/bookcase/#/ ” ) ) {
if ( ! localStorage.getItem ( " isLogin " ) ) {
  本地儲存。setItem ( “ isLogin ” , “ true ” ); //將登入狀態設為true
  本地儲存。setItem ( " uuid " , " mock_user " ); //設定假的教師UUID
  地點。重新載入（）；//重新載入網頁
}} else  if ( window .confirm ( "網站錯誤，按一下「確定」來開啟何嘉仁電子書。" )) {
  window.open ( ' https://bookonline.hess.com.tw/bookcase/#/','_blank ' ) ;
}
```
</詳情>

##可用帳號
@@ -285,19 +300,19 @@ if (window.location.href.startsWith("https://www.hle.com.tw")) {
-感謝** <ins> @foxvegajian </ins> **提供康軒網頁媒體盒的下載方法。 ( [原訊息] ( https://gist.github.com/aliyaliu368/891eef75e09494e965d291ead4a80d17?permalink_comment_id=4685986#gistcomment-4685986 ) ）
-感謝** <ins> @ J56tw </ins> **提供康軒電子書的免登入方法。( [原訊息] ( https://gist.github.com/notlin4/a05d7db77cd5606a812f4b9900fef3ee?permalink_comment_id=4788981#gistcomment-4788981 )）
-感謝** < ins > @ tmyrhs3 </ ins > **提供翰林帳號。 （[原訊息] ( https://gist.github.com/notlin4/a05d7db77cd5606a812f4b9900fef3ee?permalink_comment_id=4814684#gistcomment-4814684 )）
-趕寫** <ins> @小哲<ins>提供奇鼎事業的免登入方法（Discord ）
-最後感謝所有回答別人問題的人！

如果你覺得這篇教學對你有幫助，請點選本篇教學最上方的星星圖標，支持我繼續製作下去！

##限制
-因為本指令碼在少數網站上僅繞過了驗證，因此可能會導致無法使用儲存資料記錄、修改等功能。
-翰林版電子書每天會自動重設數據，因此需重新執行指令碼。
-翰林版電子書將於2024/6/30新增翰林帳號驗證，未來此破解方法可能無法使用，須尋找更好的解決方案。
-現有的一些指令碼有些地方的迴避方式不太好，將來也許可以用其他方式執行指令碼來交換編碼行為。

---

腳本由[ SiongSng ] ( https://github.com/SiongSng )製作，由[ notlin4 ] ( https://github.com/notlin4 )繼續| 本指令代碼由[菘菘]   ( https://github.com/SiongSng )製作，由[ notlin4 ] ( https://github.com/SiongSng )製作，由[ notlin4 ] ( https://notubub.com/not 4ub ) .
版權所有 © 2022-2024 [菘菘] ( https://github.com/SiongSng )和[ notlin4 ] ( https://github.com/notlin4 )。版權所有，並一切保留權利。  
版權所有 © 2022-2024 [菘菘] ( https://github.com/SiongSng )和[ notlin4 ] ( https://github.com/notlin4 )。保留所有權利。
版權所有 © 2022-2024 [ SiongSng ] ( https://github.com/SiongSng )和[ notlin4 ] ( https://github.com/notlin4 )。保留所有權利。
![ ] ( https://hit.yhype.me/github/profile?user_id=121224522 ) <!--觀看次數追蹤 https://yhype.me/github/profile-views -->
@notlin4 notlin4 修改了 這個要點2024年7月2日。
 修改了 1 個文件 ，新增 13 處 ， 刪除 13 處。
 26 處修改：13 處新增 & 13 處刪除二十六 
without-auth_e-book_tutorial_免登錄電子書教學.md
原始文件行號	不同行號	差異線變化
@@ -1,6 +1,6 @@
#教學用電子書及相關工具免登教學

**使用本指令碼即代表您同意本[免責聲明] ( #免責聲明)。**
**使用本指令碼即表示您同意《[免責聲明] ( #免責聲明) 》。**

##免責聲明
###將請勿將本指令碼作為抄襲答案、指向等惡意目的，使用本指令碼，請「自行承擔」一切後果與風險。
@@ -48,7 +48,​​7 @@ javascript:(function(){var script=document.createElement('script');script.src='h

###主機版
1 .前往要使用的電子書或相關工具網站。
2.按F12開啟開發人員工具，然後切換到主控台（Console）分頁。
2 .按F12開啟開發人員工具，然後切換到主控台( Console )分頁。
3 .貼上以下指令碼並執行：
``` javascript
javascript :( function ( ) { var script = document . createElement ( ' script ' ) ; script . src = ' https://cdn.jsdelivr.net/gh/notlin4/without-auth_e-book@main/fast.js '​​​​​
@@ -58,13 +58,13 @@ javascript:(function(){var script=document.createElement('script');script.src='h

![繁體中文] ( https://gist.github.com/assets/121224522/f1e71739-7a86-465b-bae5-965fcef6d23c )

如果您使用的是繁體中文（如上圖），請輸入「`允許貼上`」，然後按 Enter鍵。
如果你使用的是允許繁體中文（如上圖），請在控制台輸入「`允許貼上` ”，然後按 Enter鍵貼上。

![中文] ( https://gist.github.com/assets/121224522/11aa0d00-3684-4b16-b98a-7c0a6deff90b )

如果您使用的是英文（如上圖），請輸入「`允許貼上`」，然後按Enter鍵。
如果你使用的是中文（如上圖），請在控制台輸入「`允許貼上`」，並按下Enter鍵允許貼上。

其他語言，請輸入對應引號中的內容，然後按下Enter鍵。
對於其他語言，請在控制台輸入對應中的內容，並按下Enter鍵允許貼上。
</詳情>

4 .達成交付登錄！
@@ -75,23 +75,23 @@ javascript:(function(){var script=document.createElement('script');script.src='h

###指令碼版本
<詳細資料>
    <summary>進一步展開</summary>
    <summary>按這裡展開</summary>

1 .前往要使用的電子書或相關工具網站。
2.按F12開啟開發人員工具，然後切換到主控台（Console）分頁。
2 .按F12開啟開發人員工具，然後切換到主控台( Console )分頁。
3 .貼上下方的指令碼並執行。
<詳細資料>
    <summary>無法貼上嗎？在這裡查看如何修改</summary>

![繁體中文] ( https://gist.github.com/assets/121224522/f1e71739-7a86-465b-bae5-965fcef6d23c )

如果您使用的是繁體中文（如上圖），請輸入「`允許貼上`」，然後按 Enter鍵。
如果你使用的是允許繁體中文（如上圖），請在控制台輸入「`允許貼上` ”，然後按 Enter鍵貼上。

![中文] ( https://gist.github.com/assets/121224522/11aa0d00-3684-4b16-b98a-7c0a6deff90b )

如果您使用的是英文（如上圖），請輸入「`允許貼上`」，然後按Enter鍵。
如果你使用的是中文（如上圖），請在控制台輸入「`允許貼上`」，並按下Enter鍵允許貼上。

其他語言，請輸入對應的內容，然後按下Enter鍵。
對於其他語言，請在控制台輸入對應中的內容，並按下Enter鍵允許貼上。
</詳情>

4 .達成交付登錄！
@@ -104,7 +104,7 @@ if (window.location.href.startsWith("https://webetextbook.knsh.com.tw/")) {
  var執行=  false ;
  document.querySelectorAll ( ' .downAssetBtn ' ) .forEach ( function ( button ) {
    if ( ! executed && ( ! document.getElementById ( ' assetsPage ' ) || document.getElementById ( ' assetsPage ' ) . style.display === ' none ' ) ) {   
      alert ( '請先點選你要使用的電子書再執行指令碼。' );
      alert ( '請先點選您要使用的電子書，再執行指令碼。' );
      已執行= 真；
    } else  if ( ! executed &&  button .getAttribute ( ' d - title ' ) .includes ( " (網頁版) " )) {
      alert ( '偵測到一到五年級的內容，目前不支持繞過一到五年級的電子書，請改用網頁媒體盒進行下載。造成不便之處，我們見諒。' );
@@ -164,7 +164,7 @@ if (window.location.href.startsWith("https://edisc3.hle.com.tw/edisc_v3")) {
if ( window.location.href.includes ( “ oneclass.com.tw ” ) ) {
  讓mockToken =  JSON.stringify ( {
  “代碼”： “成功”，
  jwt ：eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJpc3MiOiJodHRwOi8vbXlhY2NvdW50Lm5hbmkuY29vbC8iLCJzdWI iOiJ1c2Vycy9rb2xhZGkxNzYyIiwiZnJvbSI6Ik5hbmkiLCJ1c2VybmFtZSI6ImtvbGFkaTE3NjIiLCJlbWFpbHZhbGl kIjp0cnVlLCJtb2JpbGV2YWxpZCI6ZmFsc2UsImVtYWlsIjoia29sYWRpMTc2MkBidXpibG94LMNvbSIsInVpZCI ​6ImZiZDY2Y2YwLTA2ZjYtMTFlZi1iNmUyLWJmYWI3YjYwOGJiMiIsImp0aSI6Ijk2YWE0ZjYzLThmYzMtNGEzMS1iMjIz LTk3YjIxZWU5NmNlNCIsImlhdCI6MTcxNDQ4NDM5MywiZXhwIjoxNzE5NjY4MzkzfQ.IG9QpMa28e2yTEBPxhtOZy3VXSAsF77KmFsRNsSo_9k ” }); 
  jwt ：eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJpc3MiOiJodHRwOi8vbXlhY2NvdW50Lm5hbmkuY29vbC8iLCJzd WIiOiJ1c2Vycy91bmljeWNsZTQiLCJmcm9tIjoiTmFuaSIsInVzZXJuYW1lIjoidW5pY3ljbGU0IiwiZW1haWx2YWxp ZCI6dHJ1ZSwibW9iaWxldmFsaWQiOmZhbHNlLCJlbWFpbCI6ImtyNTJ5NTRtQGR1Y2suY29tIiwidWlkIjoiND​ A3YzBhNjAtMzgxZS0xMWVmLWEyZjMtMGYxNmE0Y2MyYjA4IiwianRpIjoiY2FjNDAzYjAtZjkyYS00YmY1LTg0MDktN WM1OTk1OGEwMTIxIiwiaWF0IjoxNzE5ODg4ODQzLCJleHAiOjE3MjUwNzI4NDN9.-usPxm8q72YvcAkqqdRSYoxVC-h2K862EV8DCtMZQCI “ ); 
  讓欄位名稱=  " nani_oneclass_login_token " ;
  var d =  new  Date ();
  d . setTime ( d.getTime () + ( 1 * 24 *  60 * 60 * 1000  ) ) ;      
@@ -284,7 +284,7 @@ if (window.location.href.startsWith("https://www.hle.com.tw")) {
-感謝** [菘菘] ( https://github.com/SiongSng ) **製作了原始教學。 （[原教學] ( https://gist.github.com/SiongSng/baa4f015258d0312f627b5659d93d72e )已刪除，原始內容[文件] ( https://gist.github.com/tom Cheng1111/ 3c647b6b09 )於 2022/2/1），請參閱常見問題第 1 項）
-感謝** <ins> @foxvegajian </ins> **提供康軒網頁媒體盒的下載方法。 ( [原訊息] ( https://gist.github.com/aliyaliu368/891eef75e09494e965d291ead4a80d17?permalink_comment_id=4685986#gistcomment-4685986 ) ）
-感謝** <ins> @ J56tw </ins> **提供康軒電子書的免登入方法。( [原訊息] ( https://gist.github.com/notlin4/a05d7db77cd5606a812f4b9900fef3ee?permalink_comment_id=4788981#gistcomment-4788981 )）
- ** < ins > @ tmyrhs3 </ ins > ** 提供康軒總複習即測卷、翰林和南一帳號。 （感謝[原消息] ( https://gist.github.com/notlin4/a05d7db77cd5606a812f4b9900fef3ee?permalink_comment_id=4814684#gistcomment-4814684 )）
-感謝** < ins > @ tmyrhs3 </ ins > ** 提供翰林帳號。 （[原訊息] ( https://gist.github.com/notlin4/a05d7db77cd5606a812f4b9900fef3ee?permalink_comment_id=4814684#gistcomment-4814684 )）
-最後感謝所有回答別人問題的人！

如果你覺得這篇教學對你有幫助，請點選本篇教學最上方的星星圖標，支持我繼續製作下去！
@notlin4 notlin4 修改了 這個要點2024年7月2日。
 修改了 1 個文件 ，其中 新增 5 項 ， 刪除 9 項。
 14 處修改：5 處添加，9 處刪除14 
without-auth_e-book_tutorial_免登錄電子書教學.md
原始文件行號	不同行號	差異線變化
@@ -54,7 +54,7 @@ javascript:(function(){var script=document.createElement('script');script.src='h
javascript :( function ( ) { var script = document . createElement ( ' script ' ) ; script . src = ' https://cdn.jsdelivr.net/gh/notlin4/without-auth_e-book@main/fast.js '​​​​​
```
<詳細資料>
    <summary>無法貼上嗎？點我看如何修復</summary>
    <summary>無法貼上嗎？在這裡查看如何修改</summary>

![繁體中文] ( https://gist.github.com/assets/121224522/f1e71739-7a86-465b-bae5-965fcef6d23c )

@@ -81,7 +81,7 @@ javascript:(function(){var script=document.createElement('script');script.src='h
2 .按F12開啟開發人員工具，然後切換到主控台（Console）分頁。
3 .貼上下方的指令碼並執行。
<詳細資料>
    <summary>無法貼上嗎？點我看如何修復</summary>
    <summary>無法貼上嗎？在這裡查看如何修改</summary>

![繁體中文] ( https://gist.github.com/assets/121224522/f1e71739-7a86-465b-bae5-965fcef6d23c )

@@ -241,17 +241,13 @@ if (window.location.href.startsWith("https://www.hle.com.tw")) {
-密碼：` koladi1762 `

**南一**
-頭像：` Saddled7129`
-密碼：` Saddled7129`

**康軒總複習即測卷**
-帳號：` ramaw19340 `
-密碼：` a1b2c3d4 `
-帳號：`獨輪車4`
-密碼：` unicycle4`

##常見問題
**你可以在留言區提問，但在提問前請先看這裡！**
<詳細資料>
    <summary>進一步展開</summary>
    <summary>按這裡展開</summary>

1 .為什麼具體的教學不見了？
>作者本教學為因果的分支（Fork）版本，原[菘菘] ( https://github.com/SiongSng )已刪除原教學，若要查看原因請點選下方「查看原因」來展開，也請各位不要討論版權法或出版商規範的話題。
@notlin4 notlin4 修改了 這個要點2024年6月18日。
 修改了 1 個文件 ， 新增了 2 處 ， 刪除了 2 處。
 4 處修改：2 處新增 & 2 處刪除4 
without-auth_e-book_tutorial_免登錄電子書教學.md
原始文件行號	不同行號	差異線變化
@@ -241,8 +241,8 @@ if (window.location.href.startsWith("https://www.hle.com.tw")) {
-密碼：` koladi1762 `

**南一**
-帳號：` koladi1762 `
-密碼：` koladi1762 `
-頭像：` Saddled7129`
-密碼：` Saddled7129`

**康軒總複習即測卷**
-帳號：` ramaw19340 `
@notlin4 notlin4 修改了 這個要點2024年5月23日。
 修改了 1 個文件 ，新增 27 項 ， 刪除 12 項。
 39 處修改：27 處添加，12 處刪除三十九 
without-auth_e-book_tutorial_免登錄電子書教學.md
原始文件行號	不同行號	差異線變化
@@ -132,6 +132,17 @@ if (window.location.href.startsWith("https://webetextbook.knsh.com.tw/")) {
}
```

### ✅康軒總複習即測卷
連結：[康軒總複習即測卷] ( https://ttrplatform.knsh.com.tw/teacher )
``` js
if ( window.location.href.startsWith ( “ https://ttrplatform.knsh.com.tw/ ” ) ) {
  文件. cookie = “ connect.sid=s%3AXM5bGeC2DRBIbxOybL3jxaUHrWUhone4.L298aSJXZtxyUyXBV6UTk4I5rYoWAJ0OYi1VyTfl% 2BXs ”  ； 
  視窗.位置.href = “ https://ttrplatform.knsh.com.tw/teacher ” ;  
} else  if ( window .confirm ( "網站錯誤，按一下「確定」來開啟翰林行動大師。" )) {
  window.open ( ' https://ttrplatform.knsh.com.tw/teacher','_blank ' ) ;
}
```

### ✅ 翰林電子書
連結：[翰林行動大師] ( https://edisc3.hle.com.tw/edisc_v3/ebook_v2023.html )  
``` js
@@ -140,7 +151,7 @@ if (window.location.href.startsWith("https://edisc3.hle.com.tw/edisc_v3")) {
  本地儲存。setItem ( “ last_signinX_v2023 ” ,時間); //將帳號登錄日期設定為目前時間，避免被取代為過渡
  本地儲存。setItem ( " roleX_v2023 " , "老師" ); //將身分設為老師
  本地儲存。setItem ( " emailX_v2023 " , " test@test.com " ); //由於翰林電子書會驗證是否有設定郵件，只要設定即可使用
  localStorage。 O0cOsie3P40svSZXhhpNkvt-uZpdkZctVI4rl_SCYdBzniZjf25QaBRUIo0C9EHbHWOdk7G3hQ-gvwndFiz7ukku3r7pLJ97V_F-pqMWgvIgv IDrTPK0SRTYxTozhDTUXdJ20VsFQMOFbm466f2a0i6QJ4PXEjFak-qAZabOvrtG1Nuygc23xsMiDPjKdT9CnAy-biMyb-bN8CiIVECqpbFBk 45ap-1Ke_5e4pHA958vAbC9ti1aqzMCNqMyy3KwGaMitRlRM_kJ9krTB587_5ewd0GFFaiqX2jwaKZBGVJnBosrMU38d6Edue9puwMLm4TdgX2jwaKZBGVJnBosrMU38d6Edue9puwMLm4TdgX2jwaKZBGVJnBosrMU38d6Edue9puwMLm4TdgX2jwaKZBGVJnBosrMU38d6Edue9puwMLm4Tdg”）； // 設定驗證用的權限
  localStorage.setItem("tokenX_v2023", “eyJhbGciOiJSUzI1NiIsImtpZCI6Ijg1NzgwNWYxZGQ3ZmE5YTZiNTI3ZjQ0ZWNmZmJkNDhjjIiwidlw. 7YvKu2zsD4t8JoYLtUHeKopyBAb-mxneB3hU0Ejdt_-9iI-4z60_KEAnzLeBp2Gv0SSxpBgFdweRn31MIP4WHGCfpq4rPAGmdIpnWPUBTYywRcpnWPUB F7JOV_23qZIsyfXcj78K_FnBJwGuaT6J4oiyNSmuWjV7mx8tMj0IHINK3C5IJKmDDOX9ymmCk5WQ2mLuckjgel3uWoFxZTwT1mOxrVqGHmgYVo hrrt8f3YJuzLfoHxCmVQ6AW8zdc9OKi4xtaYwhHxjEOHZ5GFZ45uorWRxLIcuukdLLpUgQMl7awnL6yXbT-En7Bxzw-5v8P0WFhSI4tS8bHgSI4tS8bHg”；
  地點。重新載入（）；//重新載入網頁
} else  if ( window .confirm ( "網站錯誤，按一下「確定」來開啟翰林行動大師。" )) {
  window.open ( ' https://edisc3.hle.com.tw/edisc_v3/ebook_v2023.html','_blank ' ) ;
@@ -153,7 +164,7 @@ if (window.location.href.startsWith("https://edisc3.hle.com.tw/edisc_v3")) {
if ( window.location.href.includes ( “ oneclass.com.tw ” ) ) {
  讓mockToken =  JSON.stringify ( {
  “代碼”： “成功”，
  jwt ：eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJpc3MiOiJodHRwOi8vbXlhY2NvdW50Lm5hbmkuY29vbC8iLCJzdW IiOiJ1c2Vycy93aXRob3V0YXV0aCIsImZyb20iOiJOYW5pIiwidXNlcm5hbWUiOiJ3aXRob3V0YXV0aCIsImVtYWlsdm FsaWQiOnRydWUsIm1vYmlsZXZhbGlkIjpmYWxzZSwiZW1haWwiOiJiOWo3OWEyZ0BkdWNrLmNvbSIsInVpZCI6I ​jczOTAxNWIwLWU3OTUtMTFlZS05NGVkLWI5ZDJmNjk5NGQyZCIsImp0aSI6ImJkNTdlYzEzLTNiZDEtNDM5OS1hNTNlL TkyNzVhNDNkYzJlYyIsImlhdCI6MTcxMTAzNDAxMiwiZXhwIjoxNzE2MjE4MDEyfQ.bHi4mgrDaxlsODByZtdEWzUG17KPixEnlVoIzR2twVYY } ); 
  jwt ：eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJpc3MiOiJodHRwOi8vbXlhY2NvdW50Lm5hbmkuY29vbC8iLCJzdWI iOiJ1c2Vycy9rb2xhZGkxNzYyIiwiZnJvbSI6Ik5hbmkiLCJ1c2VybmFtZSI6ImtvbGFkaTE3NjIiLCJlbWFpbHZhbGl kIjp0cnVlLCJtb2JpbGV2YWxpZCI6ZmFsc2UsImVtYWlsIjoia29sYWRpMTc2MkBidXpibG94LMNvbSIsInVpZCI ​6ImZiZDY2Y2YwLTA2ZjYtMTFlZi1iNmUyLWJmYWI3YjYwOGJiMiIsImp0aSI6Ijk2YWE0ZjYzLThmYzMtNGEzMS1iMjIz LTk3YjIxZWU5NmNlNCIsImlhdCI6MTcxNDQ4NDM5MywiZXhwIjoxNzE5NjY4MzkzfQ.IG9QpMa28e2yTEBPxhtOZy3VXSAsF77KmFsRNsSo_9k ” }); 
  讓欄位名稱=  " nani_oneclass_login_token " ;
  var d =  new  Date ();
  d . setTime ( d.getTime () + ( 1 * 24 *  60 * 60 * 1000  ) ) ;      
@@ -177,7 +188,7 @@ if (window.location.href.includes("oneclass.com.tw")) {
``` js
if ( window.location.href.startsWith ( “ https://bookonline.hess.com.tw/bookcase/#/ ” ) ) {
if ( ! localStorage.getItem ( " isLogin " ) ) {
  本地儲存。setItem ( “ isLogin ” , “ true ” ); // 將登入狀態設為（ true ）
  本地儲存。setItem ( “ isLogin ” , “ true ” ); // 將登入狀態設為true
  本地儲存。setItem ( " uuid " , " mock_user " ); //設定假的教師UUID
  地點。重新載入（）；//重新載入網頁
}} else  if ( window .confirm ( "網站錯誤，按一下「確定」來開啟何嘉仁電子書。" )) {
@@ -189,7 +200,7 @@ if (!localStorage.getItem("isLogin")) {
連結：[翰林雲端命題大師] ( https://testbank.hle.com.tw )
``` js
if ( window.location.href.startsWith ( “ https://testbank.hle.com.tw ” ) ) {
  localStorage.setItem("oidc.user:https://id.hle.com.tw:js", '{“access_token”：“eyJhbGciOiJSUzI1NiIsImtpZCI6Ijg1NzgwNWYxZGQ3ZmE5YTZiNTI3ZjQ0ZWNmZmJkNDhjIiwidHlwIjoiNTI3ZjQ0ZWNmZmJkNDhjIiwidHlwIjoiYXQQ5901ZFXQ59 OISwQo99RwPj0mTHnb9Aod2_hDKuzqvxSXO4sIcuzNesa8WcoAJUd3ZdIgsPlIpFGxuioN xEsbWbm-sR9tv-OQUdiEuAXSAkiB_-1y5TKeUbF_nDxQ-KjwjAiwkaLqyXA2cGcpX3j2F7v J5fU8rkEqmHyjMeoRV25Qc3cqSQfqmzTbZnLfJzS7tnM00zoIPrb9NPIKnMTm0LNipFd_u AzxCGQzsal0Gyxm5Hd45Hjk4GFu2fPtOtq2U4bBjKcaRljD8LwUhMFZH_PGkuOxncZHvS8h c-Lx9YS3QgQDuOELKc6UgRsMZ7008ql7uA","id_token":"eyJhbGciOiJSUzI1NiIsIm tpZCI6Ijg1NzgwNWYxZGQ3ZmE5YTZiNTI3ZjQ0ZWNmZmJkNDhjIiwidHlwIjoiSldUIn0..PK3xCNkOkgHw-peD_QwuWH7XlPJCiMCdX5QFh_clfh31km-Bl9uLxvEkqO4VSpGgP2ZUSyoU0Y1D-xzi44Rmjy lv0GJcuIViAyU_5UgyjpxJFtB0J8NDzegnIenr3QzJPOqItWA7y4BkMMp79gjNtBwU3kEuMliIYqgdaM_pEZB_G 8nnU_1moaI-drcHejk-p_GynCmJl2HMfquxwRR66d5g9QXdYm08x3491J6COdAKgMej7mNt6Z4GnMKMamIx7gJA Dre3Hd563qHWBxSmj9MGPkl9xEvKWAEMU_jg_A6KNQICUb-B0YfD3sh4IqLi5ZkPIGZV1EuKNUoxLE6Kpw”}');
  localStorage.setItem("oidc.user:https://id.hle.com.tw:js", '{“access_token”：“eyJhbGciOiJSUzI1NiIsImtpZCI6Ijg1NzgwNWYxZGQ3ZmE5YTZiNTI3ZjQ0ZWNmZmJkNDhjIiwidHlwIjoiYXQrand0In0iYXQrand0In0 ..tRzJFMcjaxDj7YvKu2zsD4t8JoYLtUHeKopyBAb-mxneB3hU0Ejdt_-9iI-4z60_KEAnzLeBp2Gv0SSxpBgFdweRn31MIP4WHGCfpqLeBp2Gv0SSxpBgFdweRn31MIP4WHGCfpq4rPAGImd WPUBTYywRcXF7JOV_23qZIsyfXcj78K_FnBJwGuaT6J4oiyNSmuWjV7mx8tMj0IHINK3C5IJKmDDOX9ymmCk5WQ2mLuckjglel3uWoFxZTwT1mOx qGHmgYVohrrt8f3YJuzLfoHxCmVQ6AW8zdc9OKi4xtaYwhHxjEOHZ5GFZ45uorWRxLIcuukdLLpUgQMl7awnL6yXbT-En7Bxzw-5v8P0WFhSI4tS8b Hg","id_token":"eyJhbGciOiJSUzI1NiIsImtpZCI6Ijg1NzgwNWYxZGQ3ZmE5YTZiNTI3ZjQ0ZWNmZmJkNDhjIiwidHlwIjoiNTI3ZjQ0ZWNmZmJkNDhjIiwidHlwIjoiSldUIn0..cySod WB702wd4_IXGXWuwcas0m7jUL2VSCUnmHcTWKpNy7GPZTJv5FjMHVISwpViS8pxrWnKzd0YA3xCAopo7XB0_n1W8OjPb82dALd4nt-9xCAopo7XB0_n1W8OjPb82dALd4nt-9ozP0IedAOEo ji_2XoTf-TtBSCtsOFa6H6WZtRG4In8v-8fVLYrBVTdVs9mSiGAn_W7GQiI-fhbb6G3MM3ctKoPLg-0LmVELDbp0gFKNUbIQhpxIKS3M3ctIkpl3-f 2mT9OiGlgFieY6xhNpSyPCqnFA7HSvMHfJFYlgOfU2RdEJyZQSitbLYEsh-vNZrufrewpxW6Bdc4AqI4U_KXOrOoo1T7TowBWOg7dxLPHhw}'');
  地點。重新載入（）；//重新載入網頁
} else  if ( window .confirm ( "網站錯誤，按「確定」來開啟網站。" )) {
  window.open ( ' https : //testbank.hle.com.tw','_blank ' ) ;
@@ -199,7 +210,7 @@ if (window.location.href.startsWith("https://testbank.hle.com.tw")) {
連結：[翰林輔材網] ( https://reference.hle.com.tw )
``` js
if ( window.location.href.startsWith ( “ https://reference.hle.com.tw ” ) ) {
  sessionStorage.setItem("accessToken", “eyJhbGciOiJSUzI1NiIsImtpZCI6Ijg1NzgwNWYxZGQ3ZmE5YTZiNTI3ZjQ0ZWNmZmJkNDhjIiwidHlwIjoiwidHw; PPq5wOhITi3TRddTqfWq-_yHWAPf0jw9EYNWE2LTT7lkTBET-RO6dXSOOR9E7eHeXlaxwPCGKErK0JJYY_WxvgxmuARub2YiAmS2zYsHoIpBCE5 yMFkjw2HKKFQ4nMf_pQj8bazx6aYEFGRYL8K1vC8Y2omugd3igVbqF6IE7wjBg35CLiLt20aYpVYaNE8mikoCQjQ3BMIuuf_h0e61N5ZqqRUN lbJj-kjILJ2UjQ8x_5woE5ZB0kh6CJO-34ygGHcd7G17XUbuJY_Y-vuldpqexlo43SUDVmgkDiF1HkJuoEGQtzbV6auhqSHpRapN6ktJw7kw"); // 設置權杖
  sessionStorage.setItem("accessToken", “eyJhbGciOiJSUzI1NiIsImtpZCI6Ijg1NzgwNWYxZGQ3ZmE5YTZiNTI3ZjQ0ZWNmZmJkNDhjIiwFMHlwIjot 7YvKu2zsD4t8JoYLtUHeKopyBAb-mxneB3hU0Ejdt_-9iI-4z60_KEAnzLeBp2Gv0SSxpBgFdweRn31MIP4WHGCfpq4rPAGmdIpnWPUBTYywRcpnWPUB F7JOV_23qZIsyfXcj78K_FnBJwGuaT6J4oiyNSmuWjV7mx8tMj0IHINK3C5IJKmDDOX9ymmCk5WQ2mLuckjgel3uWoFxZTwT1mOxrVqGHmgYVo hrrt8f3YJuzLfoHxCmVQ6AW8zdc9OKi4xtaYwhHxjEOHZ5GFZ45uorWRxLIcuukdLLpUgQMl7awnL6yXbT-En7Bxzw-5v8P0WFhSI4tS8bHgSI4tS8bHg”）；
  會話存儲。setItem ( " userRole " , "老師" ); //將身分設為老師
  地點。重新載入（）；//重新載入網頁
} else  if ( window .confirm ( "網站錯誤，按一下「確定」來開啟翰林輔材網。 " )) {
@@ -208,29 +219,33 @@ if (window.location.href.startsWith("https://reference.hle.com.tw")) {
```

### ✅ 翰林教學資源
連結：[翰林教學資源] ( https://www.hle.com.tw / )
連結：[翰林教學資源] ( https://www.hle.com.tw )
``` js
if ( window.location.href.startsWith ( “ https://www.hle.com.tw ” ) ) {
  本地儲存。setItem ( "角色" , "老師" ); //將身分設為老師
  localStorage.setItem("令牌", “eyJhbGciOiJSUzI1NiIsImtpZCI6Ijg1NzgwNWYxZGQ3ZmE5YTZiNTI3ZjQ0ZWNmZmJkNDhjIiwidHlwIjoiwidHlwIjoi_pmg00Q 2JXixdy2GFjKIREMBZqXWgu6uAsqk-HsAV_Hl8hW5OSH0lGZ9Gp4csGJcmN-JYip-8T0ZQG22QhXgsHc3wjCd-LJ7Z00w8DNmiQG22QhXgsHc3wjCd-LJ7Z00w8DNmimiQG22QhXgsHc3wjCd-LJ7Z00w8DNmimiwww. MVKTNSsDO2I9gCZAd0BOPYpCNFXzY6TTwH6V2hKW6XJ2RvO2uq-UmeSe-lpXVFaRJ5zohoP2bnn29HSJIwDh-wyroBVIz_2uEorj2Zi8PPcBb4A Ie4Co8X3F1sQYNMzNnxjlKLpfuQpBxt3bzIPAd9XFP6h_21pzVfB4bd6JSQNX3KJ8y0t0KWzWyIBhKf7UuB69q7RXzpgg2BXVclpzpg2BXGlp7
  localStorage.setItem("令牌", “eyJhbGciOiJSUzI1NiIsImtpZCI6Ijg1NzgwNWYxZGQ3ZmE5YTZiNTI3ZjQ0ZWNmZmJkNDhjIiwidHlFMwIjoiWrandjQ0ZWNmZmJkNDhjIiwidHlFMwIjoiY 7YvKu2zsD4t8JoYLtUHeKopyBAb-mxneB3hU0Ejdt_-9iI-4z60_KEAnzLeBp2Gv0SSxpBgFdweRn31MIP4WHGCfpq4rPAGmdIpnWPUBTYywRcpnWPUB F7JOV_23qZIsyfXcj78K_FnBJwGuaT6J4oiyNSmuWjV7mx8tMj0IHINK3C5IJKmDDOX9ymmCk5WQ2mLuckjgel3uWoFxZTwT1mOxrVqGHmgYVo hrrt8f3YJuzLfoHxCmVQ6AW8zdc9OKi4xtaYwhHxjEOHZ5GFZ45uorWRxLIcuukdLLpUgQMl7awnL6yXbT-En7Bxzw-5v8P0WFhSI4tS8bHgSI4tS8bHg”；
  地點。重新載入（）；//重新載入網頁
} else  if ( window .confirm ( "網站錯誤，按「確定」來開啟網站。" )) {
  window.open ( ' https : //www.hle.com.tw','_blank ' ) ;
}
```

>最後測試時間：2024/ 3/21
>最後測試時間：2024/ 5/23
</詳情>
##可用帳號
**請勿更改以下所有帳號的個人資料！**

**翰林**
-帳號：` ramaw19340@wikfee .com `
-密碼：` a1b2c3d4 `
-帳號：` koladi1762@buzblox .com `
-密碼：` koladi1762 `

**南一**
-頭像：` Saddled7129`
-帳號：` koladi1762 `
-密碼：` koladi1762 `

**康軒總複習即測卷**
-帳號：` ramaw19340 `
-密碼：` a1b2c3d4 `

##常見問題
@@ -273,7 +288,7 @@ if (window.location.href.startsWith("https://www.hle.com.tw")) {
-感謝** [菘菘] ( https://github.com/SiongSng ) **製作了原始教學。 （[原教學] ( https://gist.github.com/SiongSng/baa4f015258d0312f627b5659d93d72e )已刪除，原始內容[文件] ( https://gist.github.com/tom Cheng1111/ 3c647b6b09 )於 2022/2/1），請參閱常見問題第 1 項）
-感謝** <ins> @foxvegajian </ins> **提供康軒網頁媒體盒的下載方法。 ( [原訊息] ( https://gist.github.com/aliyaliu368/891eef75e09494e965d291ead4a80d17?permalink_comment_id=4685986#gistcomment-4685986 ) ）
-感謝** <ins> @ J56tw </ins> **提供康軒電子書的免登入方法。( [原訊息] ( https://gist.github.com/notlin4/a05d7db77cd5606a812f4b9900fef3ee?permalink_comment_id=4788981#gistcomment-4788981 )）
-感謝** < ins > @ tmyrhs3 </ ins > ** 提供翰林與南一帳號。 （[原訊息] ( https://gist.github.com/notlin4/a05d7db77cd5606a812f4b9900fef3ee?permalink_comment_id=4814684#gistcomment-4814684 )）
- ** < ins > @ tmyrhs3 </ ins > ** 提供康軒總複習即測卷、翰林和南一帳號。 （感謝[原消息] ( https://gist.github.com/notlin4/a05d7db77cd5606a812f4b9900fef3ee?permalink_comment_id=4814684#gistcomment-4814684 )）
-最後感謝所有回答別人問題的人！

如果你覺得這篇教學對你有幫助，請點選本篇教學最上方的星星圖標，支持我繼續製作下去！
@notlin4 notlin4 修改了 這個要點2024年4月13日。
 修改了 1 個文件 ，新增 13 處 ， 刪除 13 處。
 26 處修改：13 處新增 & 13 處刪除二十六 
without-auth_e-book_tutorial_免登錄電子書教學.md
原始文件行號	不同行號	差異線變化
@@ -13,7 +13,7 @@
開發這個並不是希望拿真正的抄答案，是希望讓需要用的人可以使用，也希望各家出版社能夠提供一個學生和家長去的版本，就是只能瀏覽但不能顯示答案或者專門為學習者設計，就可以完美解決這些問題。

##如何使用
以下指令碼託管於儲存庫[ without -auth_e-book/fast.js ] ( https://github.com/notlin4/without-auth_e-book/blob/main/fast.js )，並使用[ jsDelivr ] ( https://www.jsdelivr.com/ ) 快取資源，更新日誌可於[這裡] (jsdelivr.com/ )快取資源，更新日誌可在[這裡] https://github.com/notlin4/without-auth_e-book/commits/main/fast.js ）查看。  
以下指令碼託管於儲存庫[ without -auth_e-book/fast.js ] ( https://github.com/notlin4/without-auth_e-book/blob/main/fast.js )，並使用[ jsDelivr ] ( https://www.jsdelivr.com/ ) 快取資料，更新日誌可在[這裡] (jsdelivr.com/ )快取資料，更新日誌可在[這裡] https://github.com/notlin4/without-auth_e-book/commits/main/fast.js ）查看。  
**請勿更改以下所有帳號的個人資料！**

###支援網站：
@@ -32,7 +32,7 @@ javascript:(function(){var script=document.createElement('script');script.src='h
4 .前往要使用的電子書或相關工具網站，點選書籤或在網址列輸入書籤的名稱。
5 .達成交付登錄！

如要在手機或平板電腦上使用，請輕觸「檢視方式」並遵循以下步驟操作：
如要在手機或平板電腦上使用，請輕觸「檢視方式」並遵循以下步驟操作：
<詳細資料>
    <summary>檢視方法</summary>

@@ -60,9 +60,9 @@ javascript:(function(){var script=document.createElement('script');script.src='h

如果您使用的是繁體中文（如上圖），請輸入「`允許貼上`」，然後按 Enter 鍵。

![中文] ( https://gist.github.com/assets/121224522/11aa0d00-3684-4b16-b98a-7c0a6deff90b )
![中文] ( https://gist.github.com/assets/121224522/11aa0d00-3684-4b16-b98a-7c0a6deff90b )

如果您使用的是英文（如上圖），請輸入「`允許貼上`」，然後按 Enter 鍵。
如果您使用的是英文（如上圖），請輸入「`允許貼上`」，然後按 Enter 鍵。

其他語言，請輸入對應中的內容，然後按 Enter 鍵。
</詳情>
@@ -87,9 +87,9 @@ javascript:(function(){var script=document.createElement('script');script.src='h

如果您使用的是繁體中文（如上圖），請輸入「`允許貼上`」，然後按 Enter 鍵。

![中文] ( https://gist.github.com/assets/121224522/11aa0d00-3684-4b16-b98a-7c0a6deff90b )
![中文] ( https://gist.github.com/assets/121224522/11aa0d00-3684-4b16-b98a-7c0a6deff90b )

如果您使用的是英文（如上圖），請輸入「`允許貼上`」，然後按 Enter 鍵。
如果您使用的是英文（如上圖），請輸入「`允許貼上`」，然後按 Enter 鍵。

其他語言，請輸入對應的內容，然後按 Enter 鍵。
</詳情>
@@ -98,7 +98,7 @@ javascript:(function(){var script=document.createElement('script');script.src='h

### ✅ 康軒電子書與網頁媒體盒
連結：[國小領域] ( https://webetextbook.knsh.com.tw/2/index.html?code_ Degree=1 )｜[國小英文] ( https://webetextbook.knsh.com.tw/2/index.html?code_ Degree =3 )｜[國中領域＜)｜[國中輔材] ( https://digitalmaster.knsh.com.tw/ebook/review/ )｜[網頁媒體盒] ( https://digitalmaster.knsh.com.tw/downloader/box-web/index.html )  
**注意事項**：需要先點選要下載的電子書資源，再執行指令碼才會生效，且切換電子書資源需要再執行一次。目前電子書尚未支援一到五年級內容，目前可透過網頁媒體盒下載造成不便之處，各位見諒。
**注意事項**：需要先點選要下載的電子書，再執行指令碼才會生效，且每次切換電子書都需要再執行一次。目前電子書尚未支援一到五年級的內容，可改用網頁媒體盒進行下載。造成不便之處，小見諒解。
``` js
if ( window.location.href.startsWith ( “ https://webetextbook.knsh.com.tw/ ” ) ) {
  var執行=  false ;
@@ -107,7 +107,7 @@ if (window.location.href.startsWith("https://webetextbook.knsh.com.tw/")) {
      alert ( '請先點選你要使用的電子書再執行指令碼。' );
      已執行= 真；
    } else  if ( ! executed &&  button .getAttribute ( ' d - title ' ) .includes ( " (網頁版) " )) {
      alert ( '偵測到一到五年級的內容，目前不支持繞過一到五年級的電子書。造成不便，小見諒解。' );
      alert ( '偵測到一到五年級的內容，目前不支持繞過一到五年級的電子書，請改用網頁媒體盒進行下載。造成不便之處，我們見諒。' );
      已執行= 真；
    } else  if（！執行）{
      var link =  document.createElement ( ' a ' ) ;
@@ -138,7 +138,7 @@ if (window.location.href.startsWith("https://webetextbook.knsh.com.tw/")) {
if ( window.location.href.startsWith ( “ https://edisc3.hle.com.tw/edisc_v3 ” ) ) {
  讓時間= 新的 Date（）。getTime（）。toString（）;
  本地儲存。setItem ( “ last_signinX_v2023 ” ,時間); //將帳號登錄日期設定為目前時間，避免被取代為過渡
  本地儲存。setItem ( " roleX_v2023 " , "老師" ); // 將身分設定為老師
  本地儲存。setItem ( " roleX_v2023 " , "老師" ); // 將身分設為老師
  本地儲存。setItem ( " emailX_v2023 " , " test@test.com " ); //由於翰林電子書會驗證是否有設定郵件，只要設定即可使用
  localStorage。 O0cOsie3P40svSZXhhpNkvt-uZpdkZctVI4rl_SCYdBzniZjf25QaBRUIo0C9EHbHWOdk7G3hQ-gvwndFiz7ukku3r7pLJ97V_F-pqMWgvIgv IDrTPK0SRTYxTozhDTUXdJ20VsFQMOFbm466f2a0i6QJ4PXEjFak-qAZabOvrtG1Nuygc23xsMiDPjKdT9CnAy-biMyb-bN8CiIVECqpbFBk 45ap-1Ke_5e4pHA958vAbC9ti1aqzMCNqMyy3KwGaMitRlRM_kJ9krTB587_5ewd0GFFaiqX2jwaKZBGVJnBosrMU38d6Edue9puwMLm4TdgX2jwaKZBGVJnBosrMU38d6Edue9puwMLm4TdgX2jwaKZBGVJnBosrMU38d6Edue9puwMLm4TdgX2jwaKZBGVJnBosrMU38d6Edue9puwMLm4Tdg”）； // 設定驗證用的權限
  地點。重新載入（）；//重新載入網頁
@@ -200,7 +200,7 @@ if (window.location.href.startsWith("https://testbank.hle.com.tw")) {
``` js
if ( window.location.href.startsWith ( “ https://reference.hle.com.tw ” ) ) {
  sessionStorage.setItem("accessToken", “eyJhbGciOiJSUzI1NiIsImtpZCI6Ijg1NzgwNWYxZGQ3ZmE5YTZiNTI3ZjQ0ZWNmZmJkNDhjIiwidHlwIjoiwidHw; PPq5wOhITi3TRddTqfWq-_yHWAPf0jw9EYNWE2LTT7lkTBET-RO6dXSOOR9E7eHeXlaxwPCGKErK0JJYY_WxvgxmuARub2YiAmS2zYsHoIpBCE5 yMFkjw2HKKFQ4nMf_pQj8bazx6aYEFGRYL8K1vC8Y2omugd3igVbqF6IE7wjBg35CLiLt20aYpVYaNE8mikoCQjQ3BMIuuf_h0e61N5ZqqRUN lbJj-kjILJ2UjQ8x_5woE5ZB0kh6CJO-34ygGHcd7G17XUbuJY_Y-vuldpqexlo43SUDVmgkDiF1HkJuoEGQtzbV6auhqSHpRapN6ktJw7kw"); // 設置權杖
  會話存儲。setItem ( " userRole " , "老師" ); // 將身分設定為老師
  會話存儲。setItem ( " userRole " , "老師" ); // 將身分設為老師
  地點。重新載入（）；//重新載入網頁
} else  if ( window .confirm ( "網站錯誤，按一下「確定」來開啟翰林輔材網。 " )) {
  window.open ( ' https : //reference.hle.com.tw','_blank ' ) ;
@@ -211,7 +211,7 @@ if (window.location.href.startsWith("https://reference.hle.com.tw")) {
連結：[翰林教學資源] ( https://www.hle.com.tw/ )
``` js
if ( window.location.href.startsWith ( “ https://www.hle.com.tw ” ) ) {
  本地儲存。setItem ( "角色" , "老師" ); // 將身分設定為老師
  本地儲存。setItem ( "角色" , "老師" ); // 將身分設為老師
  localStorage.setItem("令牌", “eyJhbGciOiJSUzI1NiIsImtpZCI6Ijg1NzgwNWYxZGQ3ZmE5YTZiNTI3ZjQ0ZWNmZmJkNDhjIiwidHlwIjoiwidHlwIjoi_pmg00Q 2JXixdy2GFjKIREMBZqXWgu6uAsqk-HsAV_Hl8hW5OSH0lGZ9Gp4csGJcmN-JYip-8T0ZQG22QhXgsHc3wjCd-LJ7Z00w8DNmiQG22QhXgsHc3wjCd-LJ7Z00w8DNmimiQG22QhXgsHc3wjCd-LJ7Z00w8DNmimiwww. MVKTNSsDO2I9gCZAd0BOPYpCNFXzY6TTwH6V2hKW6XJ2RvO2uq-UmeSe-lpXVFaRJ5zohoP2bnn29HSJIwDh-wyroBVIz_2uEorj2Zi8PPcBb4A Ie4Co8X3F1sQYNMzNnxjlKLpfuQpBxt3bzIPAd9XFP6h_21pzVfB4bd6JSQNX3KJ8y0t0KWzWyIBhKf7UuB69q7RXzpgg2BXVclpzpg2BXGlp7
  地點。重新載入（）；//重新載入網頁
} else  if ( window .confirm ( "網站錯誤，按「確定」來開啟網站。" )) {
@@ -230,7 +230,7 @@ if (window.location.href.startsWith("https://www.hle.com.tw")) {
-密碼：` a1b2c3d4 `

**南一**
-帳號：`未經授權`
-頭像：` Saddled7129`
-密碼：` a1b2c3d4 `

##常見問題
@@ -266,7 +266,7 @@ if (window.location.href.startsWith("https://www.hle.com.tw")) {
>由於大部分的電子書是在開啟電子書時驗證身分，直接開啟電子書的網址即可繞過驗證（可將網址儲存到書籤）；本指令碼隨時都有可能失效，請在可用時請盡快下載所需的文件。
5 .我找到了新的方法或帳號，要怎麼提供給你？
>您可以透過Discord` @ notlin4`或電子郵件iamnotlin4+gist@gmail.com來聯絡，謝謝您！ 
>您可以使用Discord帳號` @notlin4`或電子郵件iamnotlin4+gist@gmail.com 來聯繫我，謝謝您！（請不要使用電子郵件或Discord傳送發生問題等訊息）。
</詳情>
##鳴謝
@notlin4 notlin4 修改了 這個要點2024年3月24日。
 修改了 1 個文件 ，其中 新增 1 項 ， 刪除 1 項。
 2 處修改：1 處新增 & 1 處刪除2 
without-auth_e-book_tutorial_免登錄電子書教學.md
原始文件行號	不同行號	差異線變化
@@ -23,7 +23,7 @@
-  **何嘉仁**：[何嘉仁電子書櫃] ( https://bookonline.hess.com.tw/bookcase/#/ )

###書籤版
1 .如果尚未開啟書籤列請用` Ctrl + B`開啟，然後對書籤列按滑鼠右鍵，選擇「新增網頁...」。
1 .如果尚未開啟書籤列請以` Ctrl + Shift + B `開啟，然後對書籤列按滑鼠右鍵，選擇「新增網頁...」。
2 .將名稱改為您想要使用的新名稱。
3 .將網址改成以下指令碼：
``` javascript
@notlin4 notlin4 修改了 這個要點2024年3月21日。
 修改了 1 個文件 ，其中 新增 3 項 ， 刪除 3 項。
 6 處修改：3 處新增 & 3 處刪除6 
without-auth_e-book_tutorial_免登錄電子書教學.md
原始文件行號	不同行號	差異線變化
@@ -153,7 +153,7 @@ if (window.location.href.startsWith("https://edisc3.hle.com.tw/edisc_v3")) {
if ( window.location.href.includes ( “ oneclass.com.tw ” ) ) {
  讓mockToken =  JSON.stringify ( {
  “代碼”： “成功”，
  jwt： eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJpc3MiOiJodHRwOi8vbXlhY2NvdW50Lm5hbmkuY29vbC8iLCJzdWIiOiJ1c2Vycy9iJ1c wiZnJvbSI6Ik5hbmkiLCJ1c2VybmFtZSI6InJhbWF3MTkzNDAiLCJlbWFpbHZhbGlkIjp0sIVlLCJtb2JpbGV2YWxpZCI6ZmFsc2UsIVlLCJtb2JpbGV2YWxpZCI6ZmFsc2UsIVlLCJtbIjoIjoic XcxOTM0MEB3aWtmZWUuY29tIiwidWlkIjoiMGYxZDQ3ODAtYTk3Yy0xMWVlLWE5M2MtMjVlYjM1MGQ3YWNmIiwianRpIjoiNmJj0Iz​ ZjUyLTk0M2QtMzJmNDJkNmVjOTgyIiwiaWF0IjoxNzA5MzkwMzU1LCJleHAiOjE3MTQ1NzQzNTV9.JLmzjfEhH4ddpvnZESO6FSULoTbquCEM20 " });
  jwt ：eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJpc3MiOiJodHRwOi8vbXlhY2NvdW50Lm5hbmkuY29vbC8iLCJzdW IiOiJ1c2Vycy93aXRob3V0YXV0aCIsImZyb20iOiJOYW5pIiwidXNlcm5hbWUiOiJ3aXRob3V0YXV0aCIsImVtYWlsdm FsaWQiOnRydWUsIm1vYmlsZXZhbGlkIjpmYWxzZSwiZW1haWwiOiJiOWo3OWEyZ0BkdWNrLmNvbSIsInVpZCI6I ​jczOTAxNWIwLWU3OTUtMTFlZS05NGVkLWI5ZDJmNjk5NGQyZCIsImp0aSI6ImJkNTdlYzEzLTNiZDEtNDM5OS1hNTNlL TkyNzVhNDNkYzJlYyIsImlhdCI6MTcxMTAzNDAxMiwiZXhwIjoxNzE2MjE4MDEyfQ.bHi4mgrDaxlsODByZtdEWzUG17KPixEnlVoIzR2twVYY } ); 
  讓欄位名稱=  " nani_oneclass_login_token " ;
  var d =  new  Date ();
  d . setTime ( d.getTime () + ( 1 * 24 *  60 * 60 * 1000  ) ) ;      
@@ -219,7 +219,7 @@ if (window.location.href.startsWith("https://www.hle.com.tw")) {
}
```

>最後測試時間：2024/ 1/27
>最後測試時間：2024/ 3/21
</詳情>
##可用帳號
@@ -230,7 +230,7 @@ if (window.location.href.startsWith("https://www.hle.com.tw")) {
-密碼：` a1b2c3d4 `

**南一**
-帳號：` ramaw19340 `
-帳號：`未經授權`
-密碼：` a1b2c3d4 `

##常見問題
@notlin4 notlin4 修改了 這個要點2024年3月12日。
 修改了 1 個文件 ，新增 13 處 ， 刪除 13 處。
 26 處修改：13 處新增 & 13 處刪除二十六 
without-auth_e-book_tutorial_免登錄電子書教學.md
原始文件行號	不同行號	差異線變化
@@ -6,7 +6,7 @@
###將請勿將本指令碼作為抄襲答案、指向等惡意目的，使用本指令碼，請「自行承擔」一切後果與風險。

##簡介
本指令碼用於繞過台灣電子書與教學工具的前置驗證，達成所需教師帳號即可使用。
本指令碼用於繞過台灣電子書與教學工具的預設驗證即可，達成所需教師帳號使用。

##開發緣由
究竟是因為開發者忘記帶課本，但又想探究課本的資料，心血來潮研究看看電子書的驗證設計。  
@@ -19,7 +19,7 @@
###支援網站：
-  **康軒** : [國小領域] ( https://webetextbook.knsh.com.tw/2/index.html?code_ Degree=1 ) ｜[國小英語] ( https://webetextbook.knsh.com.tw/2/index.html?code_ Degree=3 ) ｜[國中領域https://webetextbook.knsh.com.tw/2/index.html?code_ Degree= 2 )｜[國中輔材] ( https://digitalmaster.knsh.com.tw/ebook/review/ ) ｜[網頁媒體盒] ( https://digitalmaster.kdownsh.com./web.kdownshbox .
-  **翰林** : [翰林行動大師] ( https://edisc3.hle.com.tw/edisc_v3/ebook_v2023.html )｜[翰林雲端命題大師] ( https://testbank.hle.com.tw )｜[翰林輔材網] ( https: //reference.hle.com.twence )｜[翰林輔材網] (h.com https://www.hle.com.tw/ )
-  **南一** : [ OneBook電子書] ( https://reader.oneclass.com.tw/bookshelf )｜[ OneBox網頁版] ( https://onebox2.oneclass.com.tw )｜[ OnePaper線上雲端出題] ( https://onepaper.oneclass.com.tw )
-  **南一** : [ NaniBook電子書] ( https://reader.oneclass.com.tw/bookshelf )｜[ NaniBox網頁版] ( https://onebox2.oneclass.com.tw )｜[ NaniPaper線上雲端出題] ( https://onepaper.oneclass.com.tw )
-  **何嘉仁**：[何嘉仁電子書櫃] ( https://bookonline.hess.com.tw/bookcase/#/ )

###書籤版
@@ -75,7 +75,7 @@ javascript:(function(){var script=document.createElement('script');script.src='h

###指令碼版本
<詳細資料>
    <summary>點此展開</summary>
    <summary>進一步展開</summary>

1 .前往要使用的電子書或相關工具網站。
2 .按F12開啟開發人員工具，然後切換到主控台（Console）分頁。
@@ -140,7 +140,7 @@ if (window.location.href.startsWith("https://edisc3.hle.com.tw/edisc_v3")) {
  本地儲存。setItem ( “ last_signinX_v2023 ” ,時間); //將帳號登錄日期設定為目前時間，避免被取代為過渡
  本地儲存。setItem ( " roleX_v2023 " , "老師" ); //將身分設定為老師
  本地儲存。setItem ( " emailX_v2023 " , " test@test.com " ); //由於翰林電子書會驗證是否有設定郵件，只要設定即可使用
  localStorage。 O0cOsie3P40svSZXhhpNkvt-uZpdkZctVI4rl_SCYdBzniZjf25QaBRUIo0C9EHbHWOdk7G3hQ-gvwndFiz7ukku3r7pLJ97V_F-pqMWgvIgv IDrTPK0SRTYxTozhDTUXdJ20VsFQMOFbm466f2a0i6QJ4PXEjFak-qAZabOvrtG1Nuygc23xsMiDPjKdT9CnAy-biMyb-bN8CiIVECqpbFBk 45ap-1Ke_5e4pHA958vAbC9ti1aqzMCNqMyy3KwGaMitRlRM_kJ9krTB587_5ewd0GFFaiqX2jwaKZBGVJnBosrMU38d6Edue9puwMLm4TdgX2jwaKZBGVJnBosrMU38d6Edue9puwMLm4TdgX2jwaKZBGVJnBosrMU38d6Edue9puwMLm4Tdg”）； // 設定身份驗證的令牌使用權
  localStorage。 O0cOsie3P40svSZXhhpNkvt-uZpdkZctVI4rl_SCYdBzniZjf25QaBRUIo0C9EHbHWOdk7G3hQ-gvwndFiz7ukku3r7pLJ97V_F-pqMWgvIgv IDrTPK0SRTYxTozhDTUXdJ20VsFQMOFbm466f2a0i6QJ4PXEjFak-qAZabOvrtG1Nuygc23xsMiDPjKdT9CnAy-biMyb-bN8CiIVECqpbFBk 45ap-1Ke_5e4pHA958vAbC9ti1aqzMCNqMyy3KwGaMitRlRM_kJ9krTB587_5ewd0GFFaiqX2jwaKZBGVJnBosrMU38d6Edue9puwMLm4TdgX2jwaKZBGVJnBosrMU38d6Edue9puwMLm4TdgX2jwaKZBGVJnBosrMU38d6Edue9puwMLm4TdgX2jwaKZBGVJnBosrMU38d6Edue9puwMLm4Tdg”）； // 設定驗證用的權限
  地點。重新載入（）；//重新載入網頁
} else  if ( window .confirm ( "網站錯誤，按一下「確定」來開啟翰林行動大師。" )) {
  window.open ( ' https://edisc3.hle.com.tw/edisc_v3/ebook_v2023.html','_blank ' ) ;
@@ -164,7 +164,7 @@ if (window.location.href.includes("oneclass.com.tw")) {
  }別的{
    文件.cookie = fieldName + “ = ” + mockToken + “ ;  ” + expires + “ ; path =/ ” ;     
  }
  本地儲存。setItem ( “ nani_tokenInfo ” ,mockToken); // 設定身份驗證用的權杖
  本地儲存。setItem ( “ nani_tokenInfo ” ,mockToken); // 設定驗證用的權限
  地點。重新載入（）；//重新載入網頁
} else  if ( confirm ( '網站錯誤，請選擇要開啟的項目：\n\n 1.NaniBook電子書\n 2.NaniBox網頁版\n 3.NaniPaper線上雲端出題' )) {
  var selectedURL = [ ' https://reader.oneclass.com.tw/bookshelf ' , ' https://onebox2.oneclass.com.tw ' , ' https://onepaper.oneclass.com.tw ' ] [ parseInt ( Prompt ( '請輸入你的選擇（輸入數字 1、2 或 3) : ' ) ; 
@@ -212,7 +212,7 @@ if (window.location.href.startsWith("https://reference.hle.com.tw")) {
``` js
if ( window.location.href.startsWith ( “ https://www.hle.com.tw ” ) ) {
  本地儲存。setItem ( "角色" , "老師" ); //將身分設定為老師
  localStorage.setItem("令牌", “eyJhbGciOiJSUzI1NiIsImtpZCI6Ijg1NzgwNWYxZGQ3ZmE5YTZiNTI3ZjQ0ZWNmZmJkNDhjIiwidHlwIjoiwidHlwIjoi_pmg00Q 2JXixdy2GFjKIREMBZqXWgu6uAsqk-HsAV_Hl8hW5OSH0lGZ9Gp4csGJcmN-JYip-8T0ZQG22QhXgsHc3wjCd-LJ7Z00w8DNmiQG22QhXgsHc3wjCd-LJ7Z00w8DNmimiQG22QhXgsHc3wjCd-LJ7Z00w8DNmimiwww. MVKTNSsDO2I9gCZAd0BOPYpCNFXzY6TTwH6V2hKW6XJ2RvO2uq-UmeSe-lpXVFaRJ5zohoP2bnn29HSJIwDh-wyroBVIz_2uEorj2Zi8PPcBb4A Ie4Co8X3F1sQYNMzNnxjlKLpfuQpBxt3bzIPAd9XFP6h_21pzVfB4bd6JSQNX3KJ8y0t0KWzWyIBhKf7UuB69q7RXzpgg2BXGlp7mgx2BXGlp7mxB69q30m
  localStorage.setItem("令牌", “eyJhbGciOiJSUzI1NiIsImtpZCI6Ijg1NzgwNWYxZGQ3ZmE5YTZiNTI3ZjQ0ZWNmZmJkNDhjIiwidHlwIjoiwidHlwIjoi_pmg00Q 2JXixdy2GFjKIREMBZqXWgu6uAsqk-HsAV_Hl8hW5OSH0lGZ9Gp4csGJcmN-JYip-8T0ZQG22QhXgsHc3wjCd-LJ7Z00w8DNmiQG22QhXgsHc3wjCd-LJ7Z00w8DNmimiQG22QhXgsHc3wjCd-LJ7Z00w8DNmimiwww. MVKTNSsDO2I9gCZAd0BOPYpCNFXzY6TTwH6V2hKW6XJ2RvO2uq-UmeSe-lpXVFaRJ5zohoP2bnn29HSJIwDh-wyroBVIz_2uEorj2Zi8PPcBb4A Ie4Co8X3F1sQYNMzNnxjlKLpfuQpBxt3bzIPAd9XFP6h_21pzVfB4bd6JSQNX3KJ8y0t0KWzWyIBhKf7UuB69q7RXzpgg2BXVclpzpg2BXGlp7
  地點。重新載入（）；//重新載入網頁
} else  if ( window .confirm ( "網站錯誤，按「確定」來開啟網站。" )) {
  window.open ( ' https : //www.hle.com.tw','_blank ' ) ;
@@ -225,18 +225,18 @@ if (window.location.href.startsWith("https://www.hle.com.tw")) {
##可用帳號
**請勿更改以下所有帳號的個人資料！**

**南一**
-帳號：` ramaw19340 `
-密碼：` a1b2c3d4 `

**翰林**
-帳號：` ramaw19340@wikfee.com `
-密碼：` a1b2c3d4 `

**南一**
-帳號：` ramaw19340 `
-密碼：` a1b2c3d4 `

##常見問題
**你可以在留言區提問，但在提問前請先看這裡！**
<詳細資料>
    <summary>點此展開</summary>
    <summary>進一步展開</summary>

1 .為什麼具體的教學不見了？
>作者本教學為因果的分支（Fork）版本，原[菘菘] ( https://github.com/SiongSng )已刪除原教學，若要查看原因請點選下方「查看原因」來展開，也請各位不要討論版權法或出版商規範的話題。
@@ -263,7 +263,7 @@ if (window.location.href.startsWith("https://www.hle.com.tw")) {
>可以留言區詢問，我會試試看。由於龍騰的驗證機制破解，且無帳號參與測試，目前無法提供。
4.如何在開啟電子書時跳過驗證？
>由於大部分的電子書是在開啟電子書時驗證身體分，直接開啟電子書的網址即可繞過身體分驗證（可將網址儲存到書籤）；本指令碼隨時都有可能失效，請在可用時請盡快下載所需的文件。
>由於大部分的電子書是在開啟電子書時驗證身分，直接開啟電子書的網址即可繞過驗證（可將網址儲存到書籤）；本指令碼隨時都有可能失效，請在可用時請盡快下載所需的文件。
5 .我找到了新的方法或帳號，要怎麼提供給你？
>您可以透過Discord` @ notlin4`或電子郵件iamnotlin4+gist@gmail.com來聯絡，謝謝您！
@@ -279,7 +279,7 @@ if (window.location.href.startsWith("https://www.hle.com.tw")) {
如果你覺得這篇教學對你有幫助，請點選本篇教學最上方的星星圖標，支持我繼續製作下去！

##限制
- 因為本指令碼在少數網站上僅繞過了驗證的身體分數驗證，因此可能會導致無法使用儲存心率、監測記錄等功能。
- 因為本指令碼在少數網站上僅繞過了驗證，因此可能會導致無法使用儲存資料記錄、修改等功能。
-翰林版電子書每天會自動重設數據，因此需重新執行指令碼。
-翰林版電子書將於2024/6/30新增翰林帳號驗證，未來此破解方法可能無法使用，須尋找更好的解決方案。
-現有的一些指令碼有些地方的迴避方式不太好，將來也許可以用其他方式執行指令碼來交換編碼行為。
@notlin4 notlin4 修改了 這個要點2024年3月10日。
 修改了 1 個文件 ， 新增了 2 處 ， 刪除了 2 處。
 4 處修改：2 處新增 & 2 處刪除4 
without-auth_e-book_tutorial_免登錄電子書教學.md
原始文件行號	不同行號	差異線變化
@@ -189,7 +189,7 @@ if (!localStorage.getItem("isLogin")) {
連結：[翰林雲端命題大師] ( https://testbank.hle.com.tw )
``` js
if ( window.location.href.startsWith ( “ https://testbank.hle.com.tw ” ) ) {
  localStorage.setItem("oidc.user:https://id.hle.com.tw:js", '{“access_token”："eyJhbGciOiJSUzI1NiIsImtpZCI6Ijg1NzgwNWYxZGQ3ZmE5YTZiNTI3ZjQ0ZWNmZmJkNDhjIiwidHlwIjoiYXQQDIn0Ii ZXhhpNkvt-uZpdkZctVI4rl_SCYdBzniZjf25QaBRUIo0C9EHbHWOdk7G3hQ-gvwndFiz7 ukku3r7pLJ97V_F-pW9WgvIKhqMIDrTPK0SRTYxTozhDTUXdJ20VsFQMOFbm466f2a0i6QJ 4PXEjFak-qAZabOvrtG1Nuygc23xsMiDPjKdT9CnAy-biMyb-bN8CiIvCqpbFBkKOVE45ap-1Ke_5e4pHA958vAbC9ti1aqzMCNqqi3KwwMCN; waKZBGVJnBosrMU38d6Edue9puwMLm4Tdg","id_token":"eyJhbGciOiJSUzI1NiIsIm tpZCI6Ijg1NzgwNWYxZGQ3ZmE5YTZiNTI3ZjQ0ZMTI3ZfZoM2vdoz_l88dbNGaciNKvTWg81Bfu_Magpn7yEyTqYSKzBdiXbBS7dA5aoXflmI1WcKBfspDK5lQSZXtkvLV Uyw5ZXNdu4x3mhJ2_LFsGSIqR2KG1mhcwvOkbrs7srAR1fKRtELuKMDrOGwv401QxrZYgSVOTcr3Ael0IkZ3RZ9 woCslN4vHOOtjZ_7bnz5Khgb94tdJK7Yu7EkESOhZiNJRdn_3VqG3CYqwtgJzVxuXhKjrZhK8xDEYfhhcjpkBP2 Mlv7VB7a-ISzysHlaxHFfP3ie91D6wiOn-JPqxHtfAQbjFXmJN9xJyJnu5By1awl7iN3Yf3f7nv8huOiBw"}');
  localStorage.setItem("oidc.user:https://id.hle.com.tw:js", '{“access_token”：“eyJhbGciOiJSUzI1NiIsImtpZCI6Ijg1NzgwNWYxZGQ3ZmE5YTZiNTI3ZjQ0ZWNmZmJkNDhjIiwidHlwIjoiNTI3ZjQ0ZWNmZmJkNDhjIiwidHlwIjoiYXQQ5901ZFXQ59 OISwQo99RwPj0mTHnb9Aod2_hDKuzqvxSXO4sIcuzNesa8WcoAJUd3ZdIgsPlIpFGxuioN xEsbWbm-sR9tv-OQUdiEuAXSAkiB_-1y5TKeUbF_nDxQ-KjwjAiwkaLqyXA2cGcpX3j2F7v J5fU8rkEqmHyjMeoRV25Qc3cqSQfqmzTbZnLfJzS7tnM00zoIPrb9NPIKnMTm0LNipFd_u AzxCGQzsal0Gyxm5Hd45Hjk4GFu2fPtOtq2U4bBjKcaRljD8LwUhMFZH_PGkuOxncZHvS8h c-Lx9YS3QgQDuOELKc6UgRsMZ7008ql7uA","id_token":"eyJhbGciOiJSUzI1NiIsIm tpZCI6Ijg1NzgwNWYxZGQ3ZmE5YTZiNTI3ZjQ0ZWNmZmJkNDhjIiwidHlwIjoiSldUIn0..PK3xCNkOkgHw-peD_QwuWH7XlPJCiMCdX5QFh_clfh31km-Bl9uLxvEkqO4VSpGgP2ZUSyoU0Y1D-xzi44Rmjy lv0GJcuIViAyU_5UgyjpxJFtB0J8NDzegnIenr3QzJPOqItWA7y4BkMMp79gjNtBwU3kEuMliIYqgdaM_pEZB_G 8nnU_1moaI-drcHejk-p_GynCmJl2HMfquxwRR66d5g9QXdYm08x3491J6COdAKgMej7mNt6Z4GnMKMamIx7gJA Dre3Hd563qHWBxSmj9MGPkl9xEvKWAEMU_jg_A6KNQICUb-B0YfD3sh4IqLi5ZkPIGZV1EuKNUoxLE6Kpw”}');
  地點。重新載入（）；//重新載入網頁
} else  if ( window .confirm ( "網站錯誤，按「確定」來開啟網站。" )) {
  window.open ( ' https : //testbank.hle.com.tw','_blank ' ) ;
@@ -287,6 +287,6 @@ if (window.location.href.startsWith("https://www.hle.com.tw")) {
---

腳本由[ SiongSng ] ( https://github.com/SiongSng )製作，由[ notlin4 ] ( https://github.com/notlin4 )繼續| 本指令代碼由[菘菘]   ( https://github.com/SiongSng )製作，由[ notlin4 ] ( https://github.com/SiongSng )製作，由[ notlin4 ] ( https://notubub.com/not 4ub ) .
版權所有 © 2022-2024 [菘菘] ( https://github.com/SiongSng )和[ notlin4 ] ( https://github.com/notlin4 )。保留一切權利。  
版權所有 © 2022-2024 [菘菘] ( https://github.com/SiongSng )和[ notlin4 ] ( https://github.com/notlin4 )。版權所有，並一切保留權利。  
版權所有 © 2022-2024 [ SiongSng ] ( https://github.com/SiongSng )和[ notlin4 ] ( https://github.com/notlin4 )。保留所有權利。
![ ] ( https://hit.yhype.me/github/profile?user_id=121224522 ) <!--觀看次數追蹤 https://yhype.me/github/profile-views -->
@notlin4 notlin4 修改了 這個要點2024年3月6日。
 修改了 1 個文件 ， 新增了 2 處 ， 刪除了 2 處。
 4 處修改：2 處新增 & 2 處刪除4 
without-auth_e-book_tutorial_免登錄電子書教學.md
原始文件行號	不同行號	差異線變化
@@ -148,7 +148,7 @@ if (window.location.href.startsWith("https://edisc3.hle.com.tw/edisc_v3")) {
```

### ✅ 南一
連結：[ OneBook電子書] ( https://reader.oneclass.com.tw/bookshelf )｜[ OneBox網頁版] ( https://onebox2.oneclass.com.tw/ )｜[ OnePaper線上雲端出題] ( https://onepaper.oneclass.com.tw/ )
連結：[ NaniBook電子書] ( https://reader.oneclass.com.tw/bookshelf )｜[ NaniBox網頁版] ( https://onebox2.oneclass.com.tw/ )｜[ NaniPaper線上雲端出題] ( https://onepaper.oneclass.com.tw/ )
``` js
if ( window.location.href.includes ( “ oneclass.com.tw ” ) ) {
  讓mockToken =  JSON.stringify ( {
@@ -166,7 +166,7 @@ if (window.location.href.includes("oneclass.com.tw")) {
  }
  本地儲存。setItem ( “ nani_tokenInfo ” ,mockToken); //設定身份驗證用的權杖
  地點。重新載入（）；//重新載入網頁
} else  if ( confirm ( '網站錯誤，請選擇要開啟的項目：\n\n 1. OneBook電子書\n 2. OneBox網頁版\n 3. OnePaper線上雲端出題' )) {
} else  if ( confirm ( '網站錯誤，請選擇要開啟的項目：\n\n 1.NaniBook電子書\ n 2.NaniBox網頁版\n 3.NaniPaper線上雲端出題' ) ) {
  var selectedURL = [ ' https://reader.oneclass.com.tw/bookshelf ' , ' https://onebox2.oneclass.com.tw ' , ' https://onepaper.oneclass.com.tw ' ] [ parseInt ( Prompt ( '請輸入你的選擇（輸入數字 1、2 或 3) : ' ) ; 
  selectedURL &&  window.open ( selectedURL , ' _blank ' ) ;
}
@notlin4 notlin4 修改了 這個要點2024年3月6日。
 修改了 1 個文件 ， 新增了 2 處 ， 刪除了 2 處。
 4 處修改：2 處新增 & 2 處刪除4 
without-auth_e-book_tutorial_免登錄電子書教學.md
原始文件行號	不同行號	差異線變化
@@ -153,7 +153,7 @@ if (window.location.href.startsWith("https://edisc3.hle.com.tw/edisc_v3")) {
if ( window.location.href.includes ( “ oneclass.com.tw ” ) ) {
  讓mockToken =  JSON.stringify ( {
  “代碼”： “成功”，
  jwt： eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJpc3MiOiJodHRwOi8vbXlhY2NvdW50Lm5hbmkuY29vbC8iLCJzdWIiOiJ1c2Vycy9iJ1c wiZnJvbSI6Ik5hbmkiLCJ1c2VybmFtZSI6InJhbWF3MTkzNDAiLCJlbWFpbHZhbGlkIjp0sIVlLCJtb2JpbGV2YWxpZCI6ZmFsc2UsIVlLCJtb2JpbGV2YWxpZCI6ZmFsc2UsIVlLCJtbIjoIjoic XcxOTM0MEB3aWtmZWUuY29tIiwidWlkIjoiMGYxZDQ3ODAtYTk3Yy0xMWVlLWE5M2MtMjVlYjM1MGQ3YWNmIiwianRpIjoiNDBlMDY0jjoiND​ ZGUyLWFkM2UtZjA0ZDg2YjQwOGIxIiwiaWF0IjoxNzA0MjA2MTA4LCJleHAiOjE3MDkzOTAxMDh9.wHRXGTai3_3B9N2SlnQpSmDyOTAxMDh9.wHRXGTai3_3B9N2SlnQpSmDy_MW5p23. " });
  jwt： eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJpc3MiOiJodHRwOi8vbXlhY2NvdW50Lm5hbmkuY29vbC8iLCJzdWIiOiJ1c2Vycy9iJ1c wiZnJvbSI6Ik5hbmkiLCJ1c2VybmFtZSI6InJhbWF3MTkzNDAiLCJlbWFpbHZhbGlkIjp0sIVlLCJtb2JpbGV2YWxpZCI6ZmFsc2UsIVlLCJtb2JpbGV2YWxpZCI6ZmFsc2UsIVlLCJtbIjoIjoic XcxOTM0MEB3aWtmZWUuY29tIiwidWlkIjoiMGYxZDQ3ODAtYTk3Yy0xMWVlLWE5M2MtMjVlYjM1MGQ3YWNmIiwianRpIjoiNmJj0Iz​ ZjUyLTk0M2QtMzJmNDJkNmVjOTgyIiwiaWF0IjoxNzA5MzkwMzU1LCJleHAiOjE3MTQ1NzQzNTV9.JLmzjfEhH4ddpvnZESO6FSULoTbquCEM20 " });
  讓欄位名稱=  " nani_oneclass_login_token " ;
  var d =  new  Date ();
  d . setTime ( d.getTime () + ( 1 * 24 *  60 * 60 * 1000  ) ) ;      
@@ -281,7 +281,7 @@ if (window.location.href.startsWith("https://www.hle.com.tw")) {
##限制
-因為本指令碼在少數網站上僅繞過了驗證的身體分數驗證，因此可能會導致無法使用儲存心率、監測記錄等功能。
-翰林版電子書每天會自動重設數據，因此需重新執行指令碼。
-翰林版電子書將於2024/6/30新增翰林帳號驗證，未來此破解方法可能無法使用，需要尋找更好的解決方案。
-翰林版電子書將於2024/6/30新增翰林帳號驗證，未來此破解方法可能無法使用，須尋找更好的解決方案。
-現有的一些指令碼有些地方的迴避方式不太好，將來也許可以用其他方式執行指令碼來交換編碼行為。

---
@notlin4 notlin4 修改了 這個要點2024年2月22日。
 修改了 1 個文件 ，其中 新增 1 項 ， 刪除 1 項。
 2 處修改：1 處新增 & 1 處刪除2 
without-auth_e-book_tutorial_免登錄電子書教學.md
原始文件行號	不同行號	差異線變化
@@ -153,7 +153,7 @@ if (window.location.href.startsWith("https://edisc3.hle.com.tw/edisc_v3")) {
if ( window.location.href.includes ( “ oneclass.com.tw ” ) ) {
  讓mockToken =  JSON.stringify ( {
  “代碼”： “成功”，
  jwt ：eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJpc3MiOiJodHRwOi8vbXlhY2NvdW50Lm5hbmkuY29vbC8iLCJzdWIiOiJ1c2Vycy9MIsZM ImZyb20iOiJOYW5pIiwidXNlcm5hbWUiOiJMZW5zODM4MCIsImVtYWlsdmFsaWQiOnRydWUsIm1vYmlsZXZhbGlkIjpmYWxzZSwiZW1AwiZMi 3J4ZkBkdWNrLmNvbSIsInVpZCI6ImNhZWEzY2EwLTZlN2QtMTFlZS05NTlhLTJmNDEzZWZhMjIxZiIsImp0aSI6Ijc0NTJmNDEzZWZhMjIxZiIsImp0aSI6Ijc0NTRhY​ 1iZmJiLWIxZjEyNzE3MjFlYSIsImlhdCI6MTcwMjk4MzkzNywiZXhwIjoxNzA4MTY3OTM3fQ.HvQkN-h8Y0n5yFgQQ​​El3cM3fQ.HvQkN-h8Y0n5yFgQQ​​El3cM8XRMp1IEno50 " }); 
  jwt： eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJpc3MiOiJodHRwOi8vbXlhY2NvdW50Lm5hbmkuY29vbC8iLCJzdWIiOiJ1c2Vycy9iJ1c wiZnJvbSI6Ik5hbmkiLCJ1c2VybmFtZSI6InJhbWF3MTkzNDAiLCJlbWFpbHZhbGlkIjp0sIVlLCJtb2JpbGV2YWxpZCI6ZmFsc2UsIVlLCJtb2JpbGV2YWxpZCI6ZmFsc2UsIVlLCJtbIjoIjoic XcxOTM0MEB3aWtmZWUuY29tIiwidWlkIjoiMGYxZDQ3ODAtYTk3Yy0xMWVlLWE5M2MtMjVlYjM1MGQ3YWNmIiwianRpIjoiNDBlMDY0jjoiND​ ZGUyLWFkM2UtZjA0ZDg2YjQwOGIxIiwiaWF0IjoxNzA0MjA2MTA4LCJleHAiOjE3MDkzOTAxMDh9.wHRXGTai3_3B9N2SlnQpSmDyOTAxMDh9.wHRXGTai3_3B9N2SlnQpSmDy_MW5p23. " });
  讓欄位名稱=  " nani_oneclass_login_token " ;
  var d =  new  Date ();
  d . setTime ( d.getTime () + ( 1 * 24 *  60 * 60 * 1000  ) ) ;      
@notlin4 notlin4 修改了 這個要點2024年2月21日。
 修改了 1 個文件 ，新增 13 處 ， 刪除 2 處。
 15 處修改：13 處新增 & 2 處刪除15 
without-auth_e-book_tutorial_免登錄電子書教學.md
原始文件行號	不同行號	差異線變化
@@ -64,7 +64,7 @@ javascript:(function(){var script=document.createElement('script');script.src='h

如果您使用的是英文（如上圖），請輸入「`允許貼上`」，然後按 Enter 鍵。

其他語言，請輸入對應的內容，然後按 Enter 鍵。
其他語言，請輸入對應中的內容，然後按 Enter 鍵。
</詳情>

4 .達成交付登錄！
@@ -222,6 +222,17 @@ if (window.location.href.startsWith("https://www.hle.com.tw")) {
>最後測試時間：2024/1/27
</詳情>
##可用帳號
**請勿更改以下所有帳號的個人資料！**

**南一**
-帳號：` ramaw19340 `
-密碼：` a1b2c3d4 `

**翰林**
-帳號：` ramaw19340@wikfee.com `
-密碼：` a1b2c3d4 `

##常見問題
**你可以在留言區提問，但在提問前請先看這裡！**
<詳細資料>
@@ -262,7 +273,7 @@ if (window.location.href.startsWith("https://www.hle.com.tw")) {
-感謝** [菘菘] ( https://github.com/SiongSng ) **製作了原始教學。 （[原教學] ( https://gist.github.com/SiongSng/baa4f015258d0312f627b5659d93d72e )已刪除，原始內容[文件] ( https://gist.github.com/tom Cheng1111/ 3c647b6b09 )於 2022/2/1），請參閱常見問題第 1 項）
-感謝** <ins> @foxvegajian </ins> **提供康軒網頁媒體盒的下載方法。 ( [原訊息] ( https://gist.github.com/aliyaliu368/891eef75e09494e965d291ead4a80d17?permalink_comment_id=4685986#gistcomment-4685986 ) ）
-感謝** <ins> @ J56tw </ins> **提供康軒電子書的免登入方法。( [原訊息] ( https://gist.github.com/notlin4/a05d7db77cd5606a812f4b9900fef3ee?permalink_comment_id=4788981#gistcomment-4788981 )）
-感謝** < ins > @ tmyrhs3 </ ins > ** 提供翰林的頭像。 （[原訊息] ( https://gist.github.com/notlin4/a05d7db77cd5606a812f4b9900fef3ee?permalink_comment_id=4814684#gistcomment-4814684 )）
-感謝** < ins > @ tmyrhs3 </ ins > ** 提供翰林與南一帳號。 （[原訊息] ( https://gist.github.com/notlin4/a05d7db77cd5606a812f4b9900fef3ee?permalink_comment_id=4814684#gistcomment-4814684 )）
-最後感謝所有回答別人問題的人！

如果你覺得這篇教學對你有幫助，請點選本篇教學最上方的星星圖標，支持我繼續製作下去！
@notlin4 notlin4 修改了 這個要點2024年1月27日。
 修改了 1 個文件 ，其中 新增 1 項 ， 刪除 1 項。
 2 處修改：1 處新增 & 1 處刪除2 
without-auth_e-book_tutorial_免登錄電子書教學.md
原始文件行號	不同行號	差異線變化
@@ -278,4 +278,4 @@ if (window.location.href.startsWith("https://www.hle.com.tw")) {
腳本由[ SiongSng ] ( https://github.com/SiongSng )製作，由[ notlin4 ] ( https://github.com/notlin4 )繼續| 本指令代碼由[菘菘]   ( https://github.com/SiongSng )製作，由[ notlin4 ] ( https://github.com/SiongSng )製作，由[ notlin4 ] ( https://notubub.com/not 4ub ) .
版權所有 © 2022-2024 [菘菘] ( https://github.com/SiongSng )和[ notlin4 ] ( https://github.com/notlin4 )。保留一切權利。  
版權所有 © 2022-2024 [ SiongSng ] ( https://github.com/SiongSng )和[ notlin4 ] ( https://github.com/notlin4 )。保留所有權利。
![ ] ( https://hit.y-hype.me/github/profile?user_id=121224522 ) <!--觀看次數追蹤https://yhype.me/github/profile-views -->
![ ] ( https://hit.yhype.me/github/profile?user_id=121224522 ) < !--觀看次數追蹤https://yhype.me/github/profile-views -->
@notlin4 notlin4 修改了 這個要點2024年1月27日。
 修改了 1 個文件 ，其中 新增 3 項 ， 刪除 3 項。
 6 處修改：3 處新增 & 3 處刪除6 
without-auth_e-book_tutorial_免登錄電子書教學.md
原始文件行號	不同行號	差異線變化
@@ -199,7 +199,7 @@ if (window.location.href.startsWith("https://testbank.hle.com.tw")) {
連結：[翰林輔材網] ( https://reference.hle.com.tw )
``` js
if ( window.location.href.startsWith ( “ https://reference.hle.com.tw ” ) ) {
  會話存儲。setItem ( “ userToken ” , “ mockToken ” ); //設定假的權杖
  sessionStorage.setItem("accessToken", “eyJhbGciOiJSUzI1NiIsImtpZCI6Ijg1NzgwNWYxZGQ3ZmE5YTZiNTI3ZjQ0ZWNmZmJkNDhjIiwidHlwIjoiwidHw; PPq5wOhITi3TRddTqfWq-_yHWAPf0jw9EYNWE2LTT7lkTBET-RO6dXSOOR9E7eHeXlaxwPCGKErK0JJYY_WxvgxmuARub2YiAmS2zYsHoIpBCE5 yMFkjw2HKKFQ4nMf_pQj8bazx6aYEFGRYL8K1vC8Y2omugd3igVbqF6IE7wjBg35CLiLt20aYpVYaNE8mikoCQjQ3BMIuuf_h0e61N5ZqqRUN lbJj-kjILJ2UjQ8x_5woE5ZB0kh6CJO-34ygGHcd7G17XUbuJY_Y-vuldpqexlo43SUDVmgkDiF1HkJuoEGQtzbV6auhqSHpRapN6ktJw7kw"); // 設置權杖
  會話存儲。setItem ( " userRole " , "老師" ); //將身分設定為老師
  地點。重新載入（）；//重新載入網頁
} else  if ( window .confirm ( "網站錯誤，按一下「確定」來開啟翰林輔材網。 " )) {
@@ -219,7 +219,7 @@ if (window.location.href.startsWith("https://www.hle.com.tw")) {
}
```

>最後測試時間：2024/1/16
>最後測試時間：2024/1/27
</詳情>
##常見問題
@@ -278,4 +278,4 @@ if (window.location.href.startsWith("https://www.hle.com.tw")) {
腳本由[ SiongSng ] ( https://github.com/SiongSng )製作，由[ notlin4 ] ( https://github.com/notlin4 )繼續| 本指令代碼由[菘菘]   ( https://github.com/SiongSng )製作，由[ notlin4 ] ( https://github.com/SiongSng )製作，由[ notlin4 ] ( https://notubub.com/not 4ub ) .
版權所有 © 2022-2024 [菘菘] ( https://github.com/SiongSng )和[ notlin4 ] ( https://github.com/notlin4 )。保留一切權利。  
版權所有 © 2022-2024 [ SiongSng ] ( https://github.com/SiongSng )和[ notlin4 ] ( https://github.com/notlin4 )。保留所有權利。
![ ] ( https://hit.yhype.me/github/profile?user_id=121224522 ) < !--觀看次數追蹤https://yhype.me/github/profile-views -->
![ ] ( https://hit.y-hype.me/github/profile?user_id=121224522 ) <!--觀看次數追蹤https://yhype.me/github/profile-views -->
@notlin4 notlin4 修改了 這個要點2024年1月16日。
 修改了 1 個文件 ，其中 新增 1 項 ， 刪除 1 項。
 2 處修改：1 處新增 & 1 處刪除2 
without-auth_e-book_tutorial_免登錄電子書教學.md
原始文件行號	不同行號	差異線變化
@@ -278,4 +278,4 @@ if (window.location.href.startsWith("https://www.hle.com.tw")) {
腳本由[ SiongSng ] ( https://github.com/SiongSng )製作，由[ notlin4 ] ( https://github.com/notlin4 )繼續| 本指令代碼由[菘菘]   ( https://github.com/SiongSng )製作，由[ notlin4 ] ( https://github.com/SiongSng )製作，由[ notlin4 ] ( https://notubub.com/not 4ub ) .
版權所有 © 2022-2024 [菘菘] ( https://github.com/SiongSng )和[ notlin4 ] ( https://github.com/notlin4 )。保留一切權利。  
版權所有 © 2022-2024 [ SiongSng ] ( https://github.com/SiongSng )和[ notlin4 ] ( https://github.com/notlin4 )。保留所有權利。
![ ] ( https://hit.y-hype.me/github/profile?user_id=121224522 ) <!--觀看次數追蹤https://yhype.me/github/profile-views -->
![ ] ( https://hit.yhype.me/github/profile?user_id=121224522 ) < !--觀看次數追蹤https://yhype.me/github/profile-views -->
@notlin4 notlin4 修改了 這個要點2024年1月16日。
 修改了 1 個文件， 新增 了 6 項內容 ， 刪除了 5 項內容。
 11 處修改：6 處添加，5 處刪除11 
without-auth_e-book_tutorial_免登錄電子書教學.md
原始文件行號	不同行號	差異線變化
@@ -76,6 +76,7 @@ javascript:(function(){var script=document.createElement('script');script.src='h
###指令碼版本
<詳細資料>
    <summary>點此展開</summary>

1 .前往要使用的電子書或相關工具網站。
2 .按F12開啟開發人員工具，然後切換到主控台（Console）分頁。
3 .貼上下方的指令碼並執行。
@@ -139,7 +140,7 @@ if (window.location.href.startsWith("https://edisc3.hle.com.tw/edisc_v3")) {
  本地儲存。setItem ( “ last_signinX_v2023 ” ,時間); //將帳號登錄日期設定為目前時間，避免被取代為過渡
  本地儲存。setItem ( " roleX_v2023 " , "老師" ); //將身分設定為老師
  本地儲存。setItem ( " emailX_v2023 " , " test@test.com " ); //由於翰林電子書會驗證是否有設定郵件，只要設定即可使用
  localStorage.setItem("tokenX_v2023", “eyJhbGciOiJSUzI1NiIsImtpZCI6Ijg1NzgwNWYxZGQ3ZmE5YTZiNTI3ZjQ0ZWNmZmJkNDhjIiwidHlwIlwIlwIlw; ULJHev9ButdBsX_lstI0sRX0D-XcOyvxkmagfipWGR5UkeT9DXV9aRAjH0VyXF1xR8ZcXyVwOfg9eSdl1vVR51CLv8pPmDaWFHDIjgIAoIevC9 IuukgcTkM34YdBgldEXoDopx4kpFxQvwtGHTbOkCm3maz6GQaxHHygNVAtlgP9MLZND1fdazsSikxpVNZL261Ib3tucd9zw1gs6aKOjKyJrnzEh JbYbcJcpuFrGLLrxCM-c4sxHvjSKgcZ0J3-nM-jL5l-ZSbLoVcufe808yOBr2UTjFHgWU_FMc2vK0zqcT7J_FbXURsoTpDBhos_MpO-OLg");
  localStorage。 O0cOsie3P40svSZXhhpNkvt-uZpdkZctVI4rl_SCYdBzniZjf25QaBRUIo0C9EHbHWOdk7G3hQ-gvwndFiz7ukku3r7pLJ97V_F-pqMWgvIgv IDrTPK0SRTYxTozhDTUXdJ20VsFQMOFbm466f2a0i6QJ4PXEjFak-qAZabOvrtG1Nuygc23xsMiDPjKdT9CnAy-biMyb-bN8CiIVECqpbFBk 45ap-1Ke_5e4pHA958vAbC9ti1aqzMCNqMyy3KwGaMitRlRM_kJ9krTB587_5ewd0GFFaiqX2jwaKZBGVJnBosrMU38d6Edue9puwMLm4TdgX2jwaKZBGVJnBosrMU38d6Edue9puwMLm4TdgX2jwaKZBGVJnBosrMU38d6Edue9puwMLm4Tdg”）； // 設定身份驗證的令牌使用權
  地點。重新載入（）；//重新載入網頁
} else  if ( window .confirm ( "網站錯誤，按一下「確定」來開啟翰林行動大師。" )) {
  window.open ( ' https://edisc3.hle.com.tw/edisc_v3/ebook_v2023.html','_blank ' ) ;
@@ -188,7 +189,7 @@ if (!localStorage.getItem("isLogin")) {
連結：[翰林雲端命題大師] ( https://testbank.hle.com.tw )
``` js
if ( window.location.href.startsWith ( “ https://testbank.hle.com.tw ” ) ) {
  localStorage.setItem("oidc.user:https://id.hle.com.tw:js", '{“access_token”：“eyJhbGciOiJSUzI1NiIsImtpZCI6Ijg1NzgwNWYxZGQ3ZmE5YTZiNTI3ZjQ0ZWNmZmJkNDhjIiwidHlwIjoiYXQrand0In0iYXQrand0In0 ..kUzuSlFgOLoDULJHev9ButdBsX_lstI0sRX0D-XcOyvxkmagfipWGR5UkeT9DXV9aRAjH0VyXF1xR8ZcXyVwOfg9eSdl1v51CLv8pVRPmDaWFHDI jgIAoI4evC9IuukgcTkM34YdBgldEXoDopx4kpFxQvwtGHTbOkCm3maz6GQaxHHygNVAtlgP9MLZND1fdazsSikxpVNZL261Ib3tucd9zw1gs6aKOjzw1gs6aKOjzw1gs6aKOjzw1gs6aKOjzw1gs6aKOjzw1gs6aKOjzw1gs6aKOjzw1gs6aKOjzw1gs6aKOjzw1gs6aKOjzw1 KyJrnzEhJbYbcJcpuFrGLLrxCM-c4sxHvjSKgcZ0J3-nM-jL5l-ZSbLoVcufe808yOBr2UTjFHgWU_FMc2vK0zqcT7J_FbXURURBr2UTjFHgWU_FMc2vK0zqcT7J_FbXURURBr2UTjFHgWU_FMc2vK0zqcT7J_FbXURURMpO-hos_LupOso Lg","id_token":"eyJhbGciOiJSUzI1NiIsImtpZCI6Ijg1NzgwNWYxZGQ3ZmE5YTZiNTI3ZjQ0ZWNmZmJkNDhjIiwidHlwIjoiNTI3ZjQ0ZWNmZmJkNDhjIiwidHlwIjoiSldUIn0..fZoMoM vdoz_l88dbNGaciNKvTWg81Bfu_Magpn7yEyTqYSKzBdiXbBS7dA5aoXflmI1WcKBfspDK5lQSZXtkvLVUyw5ZXNdu4x3mhJ2_LFsGSIqR2KG1mGSIqRw vOkbrs7srAR1fKRtELuKMDrOGwv401QxrZYgSVOtcr3Ael0IkZ3RZ9woCslN4vHOOtjZ_7bnz5Khgb94tdJK7Yu7EkESOhZiNJRdn_3VqG3CYg zVxuXhKjrZhK8xDEYfhhcjpkBP2Mlv7VB7a-ISzysHlaxHFfP3ie91D6wiOn-JPqxHtfAQbjFXmJN9xJyJnu5By1awl7iN3Yf3f7nv8huOiBw”');
  localStorage.setItem("oidc.user:https://id.hle.com.tw:js", '{“access_token”："eyJhbGciOiJSUzI1NiIsImtpZCI6Ijg1NzgwNWYxZGQ3ZmE5YTZiNTI3ZjQ0ZWNmZmJkNDhjIiwidHlwIjoiYXQQDIn0Ii ZXhhpNkvt-uZpdkZctVI4rl_SCYdBzniZjf25QaBRUIo0C9EHbHWOdk7G3hQ-gvwndFiz7 ukku3r7pLJ97V_F-pW9WgvIKhqMIDrTPK0SRTYxTozhDTUXdJ20VsFQMOFbm466f2a0i6QJ 4PXEjFak-qAZabOvrtG1Nuygc23xsMiDPjKdT9CnAy-biMyb-bN8CiIvCqpbFBkKOVE45ap-1Ke_5e4pHA958vAbC9ti1aqzMCNqqi3KwwMCN; waKZBGVJnBosrMU38d6Edue9puwMLm4Tdg","id_token":"eyJhbGciOiJSUzI1NiIsIm tpZCI6Ijg1NzgwNWYxZGQ3ZmE5YTZiNTI3ZjQ0ZMTI3ZfZoM2vdoz_l88dbNGaciNKvTWg81Bfu_Magpn7yEyTqYSKzBdiXbBS7dA5aoXflmI1WcKBfspDK5lQSZXtkvLV Uyw5ZXNdu4x3mhJ2_LFsGSIqR2KG1mhcwvOkbrs7srAR1fKRtELuKMDrOGwv401QxrZYgSVOTcr3Ael0IkZ3RZ9 woCslN4vHOOtjZ_7bnz5Khgb94tdJK7Yu7EkESOhZiNJRdn_3VqG3CYqwtgJzVxuXhKjrZhK8xDEYfhhcjpkBP2 Mlv7VB7a-ISzysHlaxHFfP3ie91D6wiOn-JPqxHtfAQbjFXmJN9xJyJnu5By1awl7iN3Yf3f7nv8huOiBw"}');
  地點。重新載入（）；//重新載入網頁
} else  if ( window .confirm ( "網站錯誤，按「確定」來開啟網站。" )) {
  window.open ( ' https : //testbank.hle.com.tw','_blank ' ) ;
@@ -218,7 +219,7 @@ if (window.location.href.startsWith("https://www.hle.com.tw")) {
}
```

>最後測試時間：2024/1/13
>最後測試時間：2024/1/16
</詳情>
##常見問題
@@ -254,7 +255,7 @@ if (window.location.href.startsWith("https://www.hle.com.tw")) {
>由於大部分的電子書是在開啟電子書時驗證身體分，直接開啟電子書的網址即可繞過身體分驗證（可將網址儲存到書籤）；本指令碼隨時都有可能失效，請在可用時請盡快下載所需的文件。
5 .我找到了新的方法或帳號，要怎麼提供給你？
>您可以透過電子郵件 iamnotlin4+gist@gmail.com來我的聯絡方式，謝謝您！
>您可以透過Discord` @ notlin4`或電子郵件iamnotlin4+gist@gmail.com來聯絡，謝謝您！ 
</詳情>
##鳴謝
@@ -277,4 +278,4 @@ if (window.location.href.startsWith("https://www.hle.com.tw")) {
腳本由[ SiongSng ] ( https://github.com/SiongSng )製作，由[ notlin4 ] ( https://github.com/notlin4 )繼續| 本指令代碼由[菘菘]   ( https://github.com/SiongSng )製作，由[ notlin4 ] ( https://github.com/SiongSng )製作，由[ notlin4 ] ( https://notubub.com/not 4ub ) .
版權所有 © 2022-2024 [菘菘] ( https://github.com/SiongSng )和[ notlin4 ] ( https://github.com/notlin4 )。保留一切權利。  
版權所有 © 2022-2024 [ SiongSng ] ( https://github.com/SiongSng )和[ notlin4 ] ( https://github.com/notlin4 )。保留所有權利。
![ ] ( https://hit.yhype.me/github/profile?user_id=121224522 ) < !--觀看次數追蹤https://yhype.me/github/profile-views -->
![ ] ( https://hit.y-hype.me/github/profile?user_id=121224522 ) <!--觀看次數追蹤https://yhype.me/github/profile-views -->
@notlin4 notlin4 修改了 這個要點2024年1月13日。
 修改了 1 個文件 ，其中 新增 1 項 ， 刪除 1 項。
 2 處修改：1 處新增 & 1 處刪除2 
without-auth_e-book_tutorial_免登錄電子書教學.md
原始文件行號	不同行號	差異線變化
@@ -218,7 +218,7 @@ if (window.location.href.startsWith("https://www.hle.com.tw")) {
}
```

>最後測試時間：2024/1/ 5
>最後測試時間：2024/1/13
</詳情>
##常見問題
@notlin4 notlin4 修改了 這個要點2024年1月13日。
 修改了 1 個文件 ，新增 7 項 ， 刪除 7 項。
 14 處修改：7 處添加，7 處刪除14 
without-auth_e-book_tutorial_免登錄電子書教學.md
原始文件行號	不同行號	差異線變化
@@ -1,6 +1,6 @@
#教學用電子書及相關工具免登教學

**使用本指令碼即代表您同意本[免責聲明] ( #免責聲明)。** 
**使用本指令碼即代表您同意本[免責聲明] ( #免責聲明)。**

##免責聲明
###將請勿將本指令碼作為抄襲答案、指向等惡意目的，使用本指令碼，請「自行承擔」一切後果與風險。
@@ -13,7 +13,7 @@
開發這個並不是希望拿真正的抄答案，是希望讓需要用的人可以使用，也希望各家出版社能夠提供一個學生和家長去的版本，就是只能瀏覽但不能顯示答案或者專門為學習者設計，就可以完美解決這些問題。

##如何使用
以下指令碼託管於儲存庫[ without -auth_e-book/fast.js ] ( https://github.com/notlin4/without-auth_e-book/blob/main/fast.js )，並使用[ jsDelivr ] ( https://www.jsdelivr.com/ )快取資源，更新日誌可於[這裡] (jsdelivr.com/ ) 快取資源，更新日誌可在[這裡] https://github.com/notlin4/without-auth_e-book/commits/main/fast.js ）查看。
以下指令碼託管於儲存庫[ without -auth_e-book/fast.js ] ( https://github.com/notlin4/without-auth_e-book/blob/main/fast.js )，並使用[ jsDelivr ] ( https://www.jsdelivr.com/ )快取資源，更新日誌可於[這裡] (jsdelivr.com/ ) 快取資源，更新日誌可在[這裡] https://github.com/notlin4/without-auth_e-book/commits/main/fast.js ）查看。  
**請勿更改以下所有帳號的個人資料！**

###支援網站：
@@ -42,7 +42,7 @@ javascript:(function(){var script=document.createElement('script');script.src='h
``` javascript
javascript :( function ( ) { var script = document . createElement ( ' script ' ) ; script . src = ' https://cdn.jsdelivr.net/gh/notlin4/without-auth_e-book@main/fast.js '​​​​​
```
4 .前往要使用電子書的網站，在網頁列中輸入書籤的名稱，輕觸它。
4 .前往要使用電子書的網站，在網頁列中輸入書籤的名稱並輕觸它。
5 .達成交付登錄！
</詳情>

@@ -97,7 +97,7 @@ javascript:(function(){var script=document.createElement('script');script.src='h

### ✅ 康軒電子書與網頁媒體盒
連結：[國小領域] ( https://webetextbook.knsh.com.tw/2/index.html?code_ Degree=1 )｜[國小英文] ( https://webetextbook.knsh.com.tw/2/index.html?code_ Degree =3 )｜[國中領域＜)｜[國中輔材] ( https://digitalmaster.knsh.com.tw/ebook/review/ )｜[網頁媒體盒] ( https://digitalmaster.knsh.com.tw/downloader/box-web/index.html )  
**注意事項**：需要先點選要下載的電子書資源，再執行指令碼才會生效，且切換電子書資源需要再執行一次。目前尚未支持網頁版，造成不便之處，小弟見諒。
**注意事項**：需要先點選要下載的電子書資源，再執行指令碼才會生效，且切換電子書資源需要再執行一次。目前電子書尚未支援一到五年級內容，目前可透過網頁媒體盒下載造成不便之處，各位見諒。
``` js
if ( window.location.href.startsWith ( “ https://webetextbook.knsh.com.tw/ ” ) ) {
  var執行=  false ;
@@ -106,7 +106,7 @@ if (window.location.href.startsWith("https://webetextbook.knsh.com.tw/")) {
      alert ( '請先點選你要使用的電子書再執行指令碼。' );
      已執行= 真；
    } else  if ( ! executed &&  button .getAttribute ( ' d - title ' ) .includes ( " (網頁版) " )) {
      alert ( '偵測到網頁版內容，目前尚未支援此功能，造成不便之處，大家見諒。' );
      alert ( '偵測到一到五年級的內容，目前不支持繞過一到五年級的電子書。造成不便，小見諒解。' );
      已執行= 真；
    } else  if（！執行）{
      var link =  document.createElement ( ' a ' ) ;
@@ -257,7 +257,7 @@ if (window.location.href.startsWith("https://www.hle.com.tw")) {
>您可以透過電子郵件iamnotlin4+gist@gmail.com來我的聯絡方式，謝謝您！
</詳情>
##銘謝
##鳴謝

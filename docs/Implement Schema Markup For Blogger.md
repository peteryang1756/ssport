# 為 Blogger 實施架構標記

在前面的指南中我們可以了解 Blogger 如何生成 xml 標記並添加佈局結構，但是我們需要一個模式標記以便在搜索引擎中快速索引。

Schema.org 是一項協作性社區活動，其使命是創建、維護和推廣 Internet、網頁、電子郵件消息等結構化數據的模式。

Schema.org 詞彙表可用於許多不同的編碼，包括 RDFa、Microdata 和 JSON-LD。這些詞彙表涵蓋了實體、實體之間的關係和動作，並且可以通過文檔完善的擴展模型輕鬆擴展。超過 1000 萬個網站使用 Schema.org 來標記他們的網頁和電子郵件消息。來自谷歌、微軟、Pinterest、Yandex 和其他公司的許多應用程序已經使用這些詞彙表來支持豐富的、可擴展的體驗。

Schema.org 詞彙表由 Google、Microsoft、Yahoo 和 Yandex 創建，由開放社區流程開發，使用public-schemaorg @ w3 。組織郵件列表和通過 GitHub。

共享的詞彙表使網站管理員和開發人員更容易決定架構並從他們的努力中獲得最大利益。正是本著這種精神，創始人和更大的社區走到了一起——提供了一個共享的模式集合。

有關詳細信息，請訪問架構。

這是一個基本的 xml 博主標記結構。

<?xml version="1.0" encoding="UTF-8" ?>
<!DOCTYPE html>
<html b:version='2' class='v2' expr:dir='data:blog.languageDirection' xmlns='http://www.w3.org/1999/xhtml' xmlns:b='http://www.google.com/2005/gml/b' xmlns:data='http://www.google.com/2005/gml/data' xmlns:expr='http://www.google.com/2005/gml/expr' xmlns:og='http://ogp.me/ns#'>
<head>
<meta charset='UTF-8'/>
<title><data:blog.title/></title>

<b:skin><![CDATA[

/* Variable definitions
=======================

]]></b:skin>

<style type='text/css'>
/*
-----------------------------------------------
Blogger Template Style
Name         : Basic Blogger Template
Designer     : Agus Purwantoro
Release      : April 2018
Version      : 1.0
License      : MIT
Email        : me@aguspurwantoro.com
-----------------------------------------------
Thanks to:
- Eric Meyer (CSS Reset)
*/

/* Eric Meyer&#39;s Reset CSS v2.0 (http://meyerweb.com/eric/tools/css/reset/)
--------------------------------------------------------------------------------------- */
html,body,div,span,applet,object,iframe,h1,h2,h3,h4,h5,h6,p,blockquote,pre,a,abbr,acronym,address,big,cite,code,del,dfn,em,img,ins,kbd,q,s,samp,small,strike,strong,sub,sup,tt,var,b,u,i,center,dl,dt,dd,ol,ul,li,fieldset,form,label,legend,table,caption,tbody,tfoot,thead,tr,th,td,article,aside,canvas,details,embed,figure,figcaption,footer,header,hgroup,menu,nav,output,ruby,section,summary,time,mark,audio,video{margin:0;padding:0;border:0;font-size:100%;font:inherit;vertical-align:baseline}article,aside,details,figcaption,figure,footer,header,hgroup,menu,nav,section{display:block}body{line-height:1}ol,ul{list-style:none}blockquote,q{quotes:none}blockquote:before,blockquote:after,q:before,q:after{content:&#39;&#39;;content:none}table{border-collapse:collapse;border-spacing:0}
</style>

</head>
<body>
<div id='wrapper'>
<header id='header-wrapper'>
<b:section class='header' id='header' maxwidgets='1'>
<b:widget id='Header1' locked='true' title='Basic Blogger Template (Header)' type='Header'></b:widget>
</b:section>
</header>
<nav id='navigation'>
<ul>
<li><a href=''>Home</a></li>
<li><a href=''>About</a></li>
</ul>
</nav>
<div class='clearfix'/>
<section id='outer-wrapper'>
<article id='article-wrapper'>
<b:section class='main' id='main'>
<b:widget id='Blog1' locked='true' title='Blog Posting' type='Blog'></b:widget>
</b:section>
</article>
</section>
<div class='clearfix'/>
<aside id='sidebar-wrapper'>
<b:section class='sidebar' id='sidebar' showaddelement='yes'></b:section>
</aside>
<div class='clearfix'/>
<footer id='footer-wrapper' itemscope='itemscope' itemtype='http://schema.org/WPFooter'>
<b:section class='footer' id='footer' showaddelement='yes'/>
<footer class='footer-left'>
Copyright &#169; &lt;script&gt;new Date().getFullYear()&gt;2010&amp;&amp;document.write(&quot;&quot;+new Date().getFullYear());&lt;/script&gt; <a href='/' rel='copyright'><data:blog.title/></a>
</footer>
<footer class='footer-right'>
Design by <a href='https://www.aguspurwantoro.com/' target='_blank' title='Blogger'>Agus Purwantoro</a>
</footer>
</footer>
</div>
</body>
</html>
我們需要向此佈局結構添加模式標記，這是 Blogger 的模式標記。

<body class='index' itemscope='itemscope' itemtype='http://schema.org/WebPage'>
<header id='header-wrapper' itemscope='itemscope' itemtype='http://schema.org/WPHeader'>
<nav id='navigation' itemscope='itemscope' itemtype='http://schema.org/SiteNavigationElement' role='navigation'>
<article id='article-wrapper' itemscope='itemscope' itemtype='http://schema.org/Blog' role='main'>
<aside id='sidebar-wrapper' itemscope='itemscope' itemtype='http://schema.org/WPSideBar'>
<footer id='footer-wrapper' itemscope='itemscope' itemtype='http://schema.org/WPFooter'>
這是帶有架構標記的最終佈局。

<?xml version="1.0" encoding="UTF-8" ?>
<!DOCTYPE html>
<html b:version='2' class='v2' expr:dir='data:blog.languageDirection' xmlns='http://www.w3.org/1999/xhtml' xmlns:b='http://www.google.com/2005/gml/b' xmlns:data='http://www.google.com/2005/gml/data' xmlns:expr='http://www.google.com/2005/gml/expr' xmlns:og='http://ogp.me/ns#'>
<head>
<meta charset='UTF-8'/>
<title><data:blog.title/></title>

<b:skin><![CDATA[

/* Variable definitions
=======================

]]></b:skin>

<style type='text/css'>
/*
-----------------------------------------------
Blogger Template Style
Name         : Basic Blogger Template
Designer     : Agus Purwantoro
Release      : April 2018
Version      : 1.0
License      : MIT
Email        : me@aguspurwantoro.com
-----------------------------------------------
Thanks to:
- Eric Meyer (CSS Reset)
*/

/* Eric Meyer&#39;s Reset CSS v2.0 (http://meyerweb.com/eric/tools/css/reset/)
--------------------------------------------------------------------------------------- */
html,body,div,span,applet,object,iframe,h1,h2,h3,h4,h5,h6,p,blockquote,pre,a,abbr,acronym,address,big,cite,code,del,dfn,em,img,ins,kbd,q,s,samp,small,strike,strong,sub,sup,tt,var,b,u,i,center,dl,dt,dd,ol,ul,li,fieldset,form,label,legend,table,caption,tbody,tfoot,thead,tr,th,td,article,aside,canvas,details,embed,figure,figcaption,footer,header,hgroup,menu,nav,output,ruby,section,summary,time,mark,audio,video{margin:0;padding:0;border:0;font-size:100%;font:inherit;vertical-align:baseline}article,aside,details,figcaption,figure,footer,header,hgroup,menu,nav,section{display:block}body{line-height:1}ol,ul{list-style:none}blockquote,q{quotes:none}blockquote:before,blockquote:after,q:before,q:after{content:&#39;&#39;;content:none}table{border-collapse:collapse;border-spacing:0}
</style>

</head>
<body class='index' itemscope='itemscope' itemtype='http://schema.org/WebPage'>
<div id='wrapper'>
<header id='header-wrapper' itemscope='itemscope' itemtype='http://schema.org/WPHeader'>
<b:section class='header' id='header' maxwidgets='1'>
<b:widget id='Header1' locked='true' title='Basic Blogger Template (Header)' type='Header'></b:widget>
</b:section>
</header>
<nav id='navigation' itemscope='itemscope' itemtype='http://schema.org/SiteNavigationElement' role='navigation'>
<ul>
<li><a href=''>Home</a></li>
<li><a href=''>About</a></li>
</ul>
</nav>
<div class='clearfix'/>
<section id='outer-wrapper'>
<article id='article-wrapper' itemscope='itemscope' itemtype='http://schema.org/Blog' role='main'>
<b:section class='main' id='main'>
<b:widget id='Blog1' locked='true' title='Blog Posting' type='Blog'></b:widget>
</b:section>
</article>
</section>
<div class='clearfix'/>
<aside id='sidebar-wrapper' itemscope='itemscope' itemtype='http://schema.org/WPSideBar'>
<b:section class='sidebar' id='sidebar' showaddelement='yes'></b:section>
</aside>
<div class='clearfix'/>
<footer id='footer-wrapper' itemscope='itemscope' itemtype='http://schema.org/WPFooter'>
<b:section class='footer' id='footer' showaddelement='yes'/>
<footer class='footer-left'>
Copyright &#169; &lt;script&gt;new Date().getFullYear()&gt;2010&amp;&amp;document.write(&quot;&quot;+new Date().getFullYear());&lt;/script&gt; <a href='/' rel='copyright'><data:blog.title/></a>
</footer>
<footer class='footer-right'>
Design by <a href='https://www.aguspurwantoro.com/' target='_blank' title='Blogger'>Agus Purwantoro</a>
</footer>
</footer>
</div>
</body>
</html>
請使用 Blogger 模板編輯器對其進行測試以查看更改，如果您想查看標記結構，請使用Google 結構化數據測試工具。

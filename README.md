weebly-newsticker
=================

javascript jquery text news ticker for the weebly platform


Javascript/jquery News Ticker for Weebly

Adapted By Phil Mora (philmora.com + toppgun.net + philippemora.net) for The Weebly Platform

e: phil@toppgun.net
t: @orsusvirtum
f: github.com/toppgun

(c) July 2014

Original Credits

Copyright 2013, jQuery.Org
Free to use under the MIT license.
http://www.opensource.org/licenses/mit-license.php

Other credits: Lea Veroux (prism.js), Nick Downie (Chart.js) and Risq (jquery.newsTicker.js)
All released under the MIT license
bootstrap.css and bootstrap.js copyrighted by twitter and released under the apache license
 


Weebly Installation Instructions
==================================

1. Upload the following files to your weebly website (Design -> HTML -> add files)

   * bootstrap.css
   * bootstrap.js
   * chart.js
   * jquery.mCustomScrollbar.min.js
   * jQuery.mousewheel.min.js
   * jquery.newsTicker.js
   * prism.js

2. Open weebly.html and Follow all instructions inlined inside 

<!--
  *
  * Instructions 1:
  *
  * Cut and Paste the following code inside main-style.css on weebly (design -> edit html)
  * anywhere within the page that will feature the newsticker
  * 
  *
  * You can change the news ticker font by modifying the "font-family" variable
  * And because of potential bootstrap.css issues conflicting with main-style.css, you may want
  * to tweak "font-size"
  *
  *
  * Examples at philmora.com and toppgun.net
  *
  *
  -->
 
//-------------------------------------------------------------
// Cut and Paste This Code Into Weebly Container Object
//-------------------------------------------------------------
 
#nt-title-container {
     /* background: #F2F2F2;*/
}

#nt-title {
}

#nt-title li {
    font-family: 'Source Sans Pro', sans-serif;
     font-weight: 100;
     font-size: 30px;
     color: #000000;
     white-space: nowrap;
     list-style: none;
     overflow: hidden;
     text-overflow: ellipsis;
}

//-------------------------------------------------------------
// End Cut And Paste
//-------------------------------------------------------------
 
  <!--
  *
  * Instructions 2:
  *
  * Cut and Paste the following code inside the <header> of the page on weebly  
  * that will feature the newsticker
  * 
  *
  -->
 
 <link rel="stylesheet" type="text/css" href="files/theme/bootstrap.css" />
 
 
 <!--
  *
  * Instructions 3:
  *
  * Cut and Paste the following code inside an HTML object
  * anywhere within the page that will feature the newsticker
  * 
  *
  * Note that the font color and size are modified in the CSS however 
  * the alignment can be modified below as well due to CSS conflicts inherent to the
  * weebly platform. You may want to do some tune up below with the row_height variable
  * depending on the font you're using and how much you've customized bootstrap.css
  *
  *
  * Examples at philmora.com and toppgun.net
  *
  * Please note that bootstrap.css has some weird effect on tablets, especially if you have
  * an animated gif background on a splash page - will fix later (November 2014)
  *
  *
  -->

<head>
<meta charset="UTF-8">
<title>Single Line Weebly News Ticker </title>
</head>

<body>

//-------------------------------------------------------------
// Cut and Paste This Code Into Weebly Container Object
//-------------------------------------------------------------

<div id="nt-title-container">
                             
<ul id="nt-title">
<li> this is news ticker line 1 </li>
<li> this is news ticker line 2 </li>
<li> this is news ticker line 3 </li>
<li> this is news ticker line 4 </li>
</ul>                             

</div>

<script src='http://code.jquery.com/jquery-1.10.2.min.js'></script>
<script src='files/theme/chart.js'></script>
<script src='files/theme/bootstrap.js'></script>
<script src='files/theme/prism.js'></script>
<script src='files/theme/jquery.mCustomScrollbar.min.js'></script>
<script src='files/theme/jquery.newsTicker.js'></script>
<script src='files/theme/jquery.mousewheel.min.js'></script>

<script>

jQuery(function($) {
     $(window).load(function(){
                 $('code.language-javascript').mCustomScrollbar();
             });
            var nt_title = $('#nt-title').newsTicker({
                row_height: 40,
                max_rows: 1,
                duration: 3000,
                pauseOnHover: 0
            });

});

</script>


//-------------------------------------------------------------
// End Cut And Paste
//-------------------------------------------------------------

<html lang="en"><head>
    <meta charset="UTF-8">
    <title></title>
<style id="system" type="text/css">h1,h2,h3,h4,h5,h6,p,blockquote {    margin: 0;    padding: 0;}body {    font-family: "Helvetica Neue", Helvetica, "Hiragino Sans GB", Arial, sans-serif;    font-size: 13px;    line-height: 18px;    color: #737373;    margin: 10px 13px 10px 13px;}a {    color: #0069d6;}a:hover {    color: #0050a3;    text-decoration: none;}a img {    border: none;}p {    margin-bottom: 9px;}h1,h2,h3,h4,h5,h6 {    color: #404040;    line-height: 36px;}h1 {    margin-bottom: 18px;    font-size: 30px;}h2 {    font-size: 24px;}h3 {    font-size: 18px;}h4 {    font-size: 16px;}h5 {    font-size: 14px;}h6 {    font-size: 13px;}hr {    margin: 0 0 19px;    border: 0;    border-bottom: 1px solid #ccc;}blockquote {    padding: 13px 13px 21px 15px;    margin-bottom: 18px;    font-family:georgia,serif;    font-style: italic;}blockquote:before {    content:"C";    font-size:40px;    margin-left:-10px;    font-family:georgia,serif;    color:#eee;}blockquote p {    font-size: 14px;    font-weight: 300;    line-height: 18px;    margin-bottom: 0;    font-style: italic;}code, pre {    font-family: Monaco, Andale Mono, Courier New, monospace;}code {    background-color: #fee9cc;    color: rgba(0, 0, 0, 0.75);    padding: 1px 3px;    font-size: 12px;    -webkit-border-radius: 3px;    -moz-border-radius: 3px;    border-radius: 3px;}pre {    display: block;    padding: 14px;    margin: 0 0 18px;    line-height: 16px;    font-size: 11px;    border: 1px solid #d9d9d9;    white-space: pre-wrap;    word-wrap: break-word;}pre code {    background-color: #fff;    color:#737373;    font-size: 11px;    padding: 0;}@media screen and (min-width: 768px) {    body {        width: 748px;        margin:10px auto;    }}</style><style id="custom" type="text/css"></style></head>
<body marginheight="0"><h1>一、修改example1使其输出三次方数</h1>
<h2>1、未修改前</h2>
<p><img src="ex1_unchange.png" alt="">
</p>
<h2>2、将dol文件夹中的build文件删除，否则任何修改对结果不会产生改变</h2>
<p><img src="figure.png" alt="">
</p>
<h2>3、将example1中的square文件中的i = i x i改成 i = i x i x i</h2>
<h2>4、进入dol中，重新编译一次：</h2>
<pre><code>ant –f build_zip.xml all</code></pre>
<h2>5、进入到build/bin/main，中重新运行一次，得到如图结果：</h2>
<pre><code>Sudo ant –f runexample.xml –Dnumber=1</code></pre>
<p>运行结果如图所示：
<img src="figure2.png" alt="">
</p>
<h1>二、修改example2,让3个square模块变成两个</h1>
<h2>1、打开example2.xml文件</h2>
<h2>2、将example2.xml文件中的value = 3改为value=2</h2>
<p><img src="figure3.png" alt="">

</p>
<h2>3、将dol文件中的build文件删除</h2>
<h2>4、在dol下重新编译</h2>
<pre><code>ant –f build_zip.xml all</code></pre>
<h2>5、进入build/bin/main目录下，运行：</h2>
<pre><code>sudo ant –f runexample.xml –Dnumber=2</code></pre>
<p>得到如图结果：
<img src="figure4.png" alt="">
</p>
<h2>6、查看example2.dot图</h2>
<p><img src="figure5.png" alt="">
</p>
<h1>三、实验感想</h1>
<p>   在本次实验中，要注意的地方有两点：第一个就是将build文件删除，我原先是没有将它删除的，然后，不管我对i进行怎样的更改，运行的结果仍然是原始的结果；第二个就是在删减square模块时，不需要修改端口。Square是迭代生成的，所以value是决定模块数量的最根本的变量。而当我尝试去修改origin和target的时候，就会报错，给出一个路径，并说明这个路径不存在。

</p>
<p>Edit By <a href="http://mahua.jser.me">MaHua</a></p>
</body></html>
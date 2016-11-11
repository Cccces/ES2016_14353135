<html lang="en"><head>
    <meta charset="UTF-8">
    <title></title>
<style id="system" type="text/css">h1,h2,h3,h4,h5,h6,p,blockquote {    margin: 0;    padding: 0;}body {    font-family: "Helvetica Neue", Helvetica, "Hiragino Sans GB", Arial, sans-serif;    font-size: 13px;    line-height: 18px;    color: #737373;    margin: 10px 13px 10px 13px;}a {    color: #0069d6;}a:hover {    color: #0050a3;    text-decoration: none;}a img {    border: none;}p {    margin-bottom: 9px;}h1,h2,h3,h4,h5,h6 {    color: #404040;    line-height: 36px;}h1 {    margin-bottom: 18px;    font-size: 30px;}h2 {    font-size: 24px;}h3 {    font-size: 18px;}h4 {    font-size: 16px;}h5 {    font-size: 14px;}h6 {    font-size: 13px;}hr {    margin: 0 0 19px;    border: 0;    border-bottom: 1px solid #ccc;}blockquote {    padding: 13px 13px 21px 15px;    margin-bottom: 18px;    font-family:georgia,serif;    font-style: italic;}blockquote:before {    content:"C";    font-size:40px;    margin-left:-10px;    font-family:georgia,serif;    color:#eee;}blockquote p {    font-size: 14px;    font-weight: 300;    line-height: 18px;    margin-bottom: 0;    font-style: italic;}code, pre {    font-family: Monaco, Andale Mono, Courier New, monospace;}code {    background-color: #fee9cc;    color: rgba(0, 0, 0, 0.75);    padding: 1px 3px;    font-size: 12px;    -webkit-border-radius: 3px;    -moz-border-radius: 3px;    border-radius: 3px;}pre {    display: block;    padding: 14px;    margin: 0 0 18px;    line-height: 16px;    font-size: 11px;    border: 1px solid #d9d9d9;    white-space: pre-wrap;    word-wrap: break-word;}pre code {    background-color: #fff;    color:#737373;    font-size: 11px;    padding: 0;}@media screen and (min-width: 768px) {    body {        width: 748px;        margin:10px auto;    }}</style><style id="custom" type="text/css"></style></head>
<body marginheight="0"><h1>实验五：配置Ros</h1>
<h2>一、Installation</h2>
<h3>1.Setup source list</h3>
<pre><code>sudo sh -c 'echo "deb http://packages.ros.org/ros/ubuntu $(lsb_release -sc) main" &gt; /etc/apt/sources.list.d/ros-latest.list'</code></pre>
<h3>2.set up keys</h3>
<pre><code>sudo apt-key adv --keyserver hkp://ha.pool.sks-keyservers.net:80 --recv-key 0xB01FA116</code></pre>
<h3>3.installation</h3>
<pre><code>sudo apt-get update</code></pre>
<h4>select Desktop full install</h4>
<pre><code>sudo apt-get install ros-jade-desktop-full</code></pre>
<h4>To find available packages, use:</h4>
<pre><code>apt-cache search ros-jade</code></pre>
<h3>4.Initailize rosdep</h3>
<pre><code>sudo rosdep init
rosdep update</code></pre>
<h3>5.setup environment</h3>
<pre><code>echo "source /opt/ros/jade/setup.bash" &gt;&gt; ~/.bashrc
source ~/.bashrc</code></pre>
<h3>6.getting rosinstall</h3>
<pre><code>sudo apt-get install python-rosinstall</code></pre>
<h4>最后的一部分：</h4>
<p><img src="last.png" alt="">

</p>
<h2>二、Test for ros</h2>
<h3>1.打开终端，输入</h3>
<pre><code>roscore</code></pre>
<h4>结果如图：</h4>
<p><img src="result1.png" alt="">

</p>
<h3>2.打开第二个终端，输入：</h3>
<pre><code>rosrun turtlesim turtlesim_node</code></pre>
<p><img src="fig.png" alt="">

</p>
<h4>可以看见一个有小乌龟的界面：</h4>
<p><img src="result2.png" alt="">
</p>
<h3>3.打开第三个终端，输入：</h3>
<pre><code>rosrun turtlesim turtle_teleop_key</code></pre>
<h4>读入键盘输入值，对小乌龟进行操作。</h4>
<h4>左箭头和右箭头表示方向，向上和向下箭头表示前进和后退，如图：</h4>
<p><img src="result3.png" alt="">



</p>
<p>Edit By <a href="http://mahua.jser.me">MaHua</a></p>
</body></html>
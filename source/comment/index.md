---
title: comment
date: 2018-12-20 23:13:48
keywords: 留言板
description: 
comments: true
photos: https://cdn.jsdelivr.net/gh/Eutopun/CDN@v0.75/img/banner/comment.jpg
---
{% raw %}
<div class="entry-content">
  <div class="poem-wrap">
    <div class="poem-border poem-left">
    </div>
    <div class="poem-border poem-right">
    </div>
    <h1>
    一言</h1>
	<p id="hitokoto" > 在不同的遭遇里我发现你的瞬间，有种不可言说的温柔直觉。 </p>
    <p align="right" id="afrom">
    </p>
  </div>
</div>
<script>fetch('https://v1.hitokoto.cn').then(function(res){
    return res.json();
  }).then(function (data) {
    var hitokoto = document.getElementById('hitokoto');
    var afrom = document.getElementById('afrom');
    hitokoto.innerText = data.hitokoto;
    afrom.innerText =  '——【' + data.from + '】';
  })
  .catch(function (err) {
    console.error(err);
    })</script>
{% endraw %}
## adsense-under-header.html

```html
<script async src="//pagead2.googlesyndication.com/pagead/js/adsbygoogle.js"></script>
<!-- Under Header -->
<ins class="adsbygoogle"
   style="display:block"
   data-ad-client="{{site.adsense-data-ad-client}}"
   data-ad-slot="{{site.adsense-data-ad-slot}}"
   data-ad-format="auto"
   data-full-width-responsive="true"></ins>
<script>
(adsbygoogle = window.adsbygoogle || []).push({});
</script>
<br/>
```

## default.html

`</head>`

```html
{% if jekyll.environment == 'production' %}
<!-- change your GA id in _config.yml -->
<script>
(function(i,s,o,g,r,a,m){i['GoogleAnalyticsObject']=r;i[r]=i[r]||function(){
(i[r].q=i[r].q||[]).push(arguments)},i[r].l=1*new Date();a=s.createElement(o),
m=s.getElementsByTagName(o)[0];a.async=1;a.src=g;m.parentNode.insertBefore(a,m)
})(window,document,'script','//www.google-analytics.com/analytics.js','ga');
ga('create', '{{site.google_analytics}}', 'auto');
ga('send', 'pageview');
</script>
{% endif %}
```

`<h1 class="sitetitle">{{ site.name }}</h1>`

```html
    <p class="lead">
        {{ site.description }}
    </p>
```

## disqus.html

```html
<a href="http://disqus.com" class="dsq-brlink">Sistem komentar diberdayakan oleh <span class="logo-disqus">Disqus</span>.</a>
</section>
```

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

```html
<!-- Categories Jumbotron
================================================== -->
<div class="jumbotron fortags">
	<div class="d-md-flex h-100">
		<div class="col-md-4 transpdark align-self-center text-center h-100">
            <div class="d-md-flex align-items-center justify-content-center h-100">
                <h2 class="d-md-block align-self-center py-1 font-weight-light">Jelajahi Kategori <span class="d-none d-md-inline">→</span></h2>
            </div>
		</div>
		<div class="col-md-8 p-5 align-self-center text-center">
            {% assign categories_list = site.categories %}
            {% if categories_list.first[0] == null %}
                {% for category in categories_list %}
                    <a class="mt-1 mb-1" href="{{site.baseurl}}/categories#{{ category | url_escape | strip | replace: ' ', '-' }}">{{ category | camelcase }} ({{ site.tags[category].size }})</a>
                {% endfor %}
            {% else %}
                {% for category in categories_list %}
                    <a class="mt-1 mb-1" href="{{site.baseurl}}/categories#{{ category[0] | url_escape | strip | replace: ' ', '-' }}">{{ category[0] | camelcase }} ({{ category[1].size }})</a>
                {% endfor %}
            {% endif %}
            {% assign categories_list = nil %}
		</div>
	</div>
</div>
```

```html
{% if site.mailchimp-list %}
<!-- Bottom Alert Bar
================================================== -->
<div class="alertbar">
	<div class="container text-center">
		<span><img src="{{ site.baseurl }}/{{ site.logo }}" alt="{{site.title}}"> &nbsp; Never miss a <b>story</b> from us, subscribe to our newsletter</span>
        <form action="{{site.mailchimp-list}}" method="post" name="mc-embedded-subscribe-form" class="wj-contact-form validate" target="_blank" novalidate>
            <div class="mc-field-group">
            <input type="email" placeholder="Email" name="EMAIL" class="required email" id="mce-EMAIL" autocomplete="on" required>
            <input type="submit" value="Subscribe" name="subscribe" class="heart">
            </div>
        </form>
	</div>
</div>
{% endif %}
```

## disqus.html

```html
<a href="http://disqus.com" class="dsq-brlink">Sistem komentar diberdayakan oleh <span class="logo-disqus">Disqus</span>.</a>
</section>
```

## post.html

```html
<!-- Begin Comments
==================================================
{% if page.comments != false %}
    <div class="container">
        <div id="comments" class="row justify-content-center mb-5">
            <div class="col-md-8">
                {% include comments.html %}
            </div>
        </div>
    </div>
{% endif %}
End Comments
================================================== -->

<!-- Review with LD-JSON, adapt it for your needs if you like, but make sure you test the generated HTML source code first: 
https://search.google.com/structured-data/testing-tool/u/0/
================================================== -->
```

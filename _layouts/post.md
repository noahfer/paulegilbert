---
layout: default
---
<header id="hidden-header">
	{% include post-header.html %}
</header>
<header id="top-header">
	{% include post-header.html %}
</header>
<main>
	<section class="img-container">
		{% for i in (1..page.img-count) %}
			<div class="img" class="fade" data-delay="0.0s" style="background-image: url(img/{{ page.short }}/{{ i }}.jpg);"></div>
		{% endfor %}
	</section>
	<section>	
		<h2 class="meta">{{ page.date | date_to_string | split: " " | last }}</h2>
		<h2>{{ page.title }}</h2>
		<div class="post">
			{{ content }}
		</div>
	</section>
</main>
<div id="portfolio">
	<section>
		<h2>Voir aussi</h2>
	</section>
</div>
<script>
	// When the user scrolls down 20px from the top of the document, slide down the hidden header
	window.onscroll = function() {scrollFunction()};

	function scrollFunction() {
		if (document.body.scrollTop > 20 || document.documentElement.scrollTop > 20) {
	    	document.getElementById("hidden-header").style.top = "0";
		} else {
	    	document.getElementById("hidden-header").style.top = "-60px";
		}
	}
</script>
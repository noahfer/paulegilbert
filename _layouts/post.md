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
	<section>
		<div class="image"></div>
	</section>
	<section>	
		<h2>{{ page.title }}</h2>
		<p class="meta">{{ page.date | date_to_string | split: " " | last }}</p>
		<div class="post">
			{{ content }}
		</div>
	</section>
</main>
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
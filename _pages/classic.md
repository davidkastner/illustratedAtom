---
title: Classical Artwork
subtitle: David W. Kastner
---

<section class="portfolio">

	<div class="content-wrap portfolio-wrap">

		{% for project in site.classic reversed %}

		<div class="portfolio-item">

			<a class="portfolio-item__link" href="{{ project.url | relative_url }}">

				<div class="portfolio-item__image">
					<img src="{{ project.featured_image | relative_url }}" alt="{{ project.title }}">
				</div>

				<div class="portfolio-item__content">
					<div class="portfolio-item__info">
						<h2 class="portfolio-item__title">{{ project.title }}</h2>
						<p class="portfolio-item__subtitle">{{ project.subtitle }}</p>
						{% if project.icon %}
						<div class="portfolio-item__icon"><i class="{{ project.icon }}"></i></div>
						{% endif %}
					</div>
				</div>

			</a>

		</div>

		{% endfor %}

	</div>

</section>


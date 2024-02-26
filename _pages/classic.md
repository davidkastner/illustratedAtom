---
layout: default
title: Illustrated Atom
description:
featured_image: /images/social.jpg
---

<section class="portfolio">

	<div class="content-wrap portfolio-wrap">

		{% for project in site.projects reversed %}

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

{% if paginator.total_pages > 1 %}

<section class="pagination">

	{% if paginator.previous_page %}
	<div class="pagination__prev">
		<a href="{{ paginator.previous_page_path | relative_url }}" class="button button--large"><i class="fa fa-angle-left" aria-hidden="true"></i> <span>Newer Posts</span></a>
	</div>
	{% endif %}
	{% if paginator.next_page %}
	<div class="pagination__next">
		<a href="{{ paginator.next_page_path | relative_url }}" class="button button--large"><span>Older Posts</span> <i class="fa fa-angle-right" aria-hidden="true"></i></a>
	</div>
	{% endif %}

</section>

{% endif %}

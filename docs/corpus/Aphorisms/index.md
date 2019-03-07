		{% assign mydocs = site.pages | group_by: 'section_name' %}
		{% for cat in mydocs %}
			{% if cat.name == "Aphorisms" %}
			<h2>{{ cat.name | capitalize }}</h2>
			<ul>
			  {% assign items = cat.items | sort: 'article_name' %}
			  {% for item in items %}
				<li><a href="//sepher-ehben{{ item.url }}">{{ item.article_name }}</a></li>
			  {% endfor %}
			</ul>
			{% endif %}
		{% endfor %}

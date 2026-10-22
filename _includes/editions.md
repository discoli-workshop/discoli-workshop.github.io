{%- for edition in site.data.editions %}
- **[{{ edition.id }} edition: {{ edition.name }}]({{ edition.id | prepend: "/" | append: "/" | absolute_url }})**, co-located with the [{{ edition.conference }}]({{ edition.conference_url }}) that will take place in {{ edition.venue }}.
{%- endfor %}

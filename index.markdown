---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: home
---

{% for company in site.companies %}
  <h2>{{ company.name }} - {{ company.type }}</h2>
  <a href="{{ company.url-careers }}" target='blank'>Link</a>
{% endfor %}

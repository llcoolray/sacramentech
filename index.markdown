---
layout: home
---
<section class="co-grid">

  {% for company in site.companies %}
  <div class="co-card">
    <div class="co-img">
      <img src="{{ company.image | default: "assets/defaults/img.png"  }}" alt="{{ company.name }}"  />
    </div>
    <div class="co-logo">
      <img src="{{ company.logo | default: "assets/defaults/logo.png"  }}" alt="{{ company.name }} logo" />
    </div>

    <div class="content">
      <h2>{{ company.name }}</h2>
      <h4>{{ company.type }}</h4>

      {%- if company.url-careers -%}
        <a href="{{ company.url-careers }}" target='blank'>Link</a>
      {%- endif -%}

      {%- if company.contact -%}
        <a href="mailto:{{ company.contact }}" target='blank'>Email</a>
      {%- endif -%}

      {{ company.content }}
    </div>
    
  </div>
  {% endfor %}

</section>

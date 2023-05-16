# breadcrumb

  <span aria-hidden="true">&rsaquo;</span>
    {% if current_tags %}
      {% capture url %}/collections/{{ collection.handle }}{% endcapture %}
      {{ collection.title | link_to: url }}
      <span aria-hidden="true">&rsaquo;</span>
      <span>{{ current_tags | join: " + " | replace: 'custom', 'Custom Built by Midwestern Craftsman' | replace: 'chalk/clay paint', 'Junk Gypsy™ Chalk/Clay Paint' | replace: "Milk Paint", "Miss Mustard Seed's Milk Paint" }}</span>
    {% else %}
      <span>{{ collection.title }}</span>
    {% endif %}
      <span aria-hidden="true">&rsaquo;</span>
        {% for tag in collection.tags %}
          {% if product.tags contains tag %}
            <span>{{ tag | uppercase }}</span>
          {% endif %}
        {% endfor %}
      <span aria-hidden="true">&rsaquo;</span>
      <span>{{ product.title }}</span>



https://ideawrights.com/shopify-breadcrumbs-based-on-menu-structure/

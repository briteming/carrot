{% for SITE in SITES %}

### {{SITE.class_name}}

{% if SITE.describe %}
> {{ SITE.describe }}
> {% endif %}

<table>
{% for item in SITE.datas %}
  <tr>
    <td>{{item.index}}.</td>
    <td><img src="{{item.favicon}}" alt="favicon" style="height: 20px !important;width: 20px !important;" ></td>
    <td><a href="{{item.url }}" target="_blank"> {{item.domain}} </a> </td>
    <td>{{item.content}}</td>
    <td>{{item.note}}</td> 
    <td><a href="{{item.url }}" target="_blank">🔗 </a> </td> 
  </tr>
{% endfor %}
</table>
{% endfor %}


#### 失效站点

<details>
  <summary>失效站点</summary>

{% for item in items_shi_xiao %}
{{item.index}}. {{ item.url }} <br/>
{% endfor %}

</details>
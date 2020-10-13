{
    "title": "Categories",
    "sidebar": true,
    "weight": "1"
}



{{ $categories := .Params.categories }}
<ul>
{{ range $key, $taxonomy := .Site.Taxonomies.categories }}
  {{ if eq $key $categories }}
    {{ range $taxonomy.Pages }}
    <li><a href="{{ .Permalink }}">{{ .Title }}</a></li>
    {{ end }}
  {{ end }}
{{ end }}
</ul>

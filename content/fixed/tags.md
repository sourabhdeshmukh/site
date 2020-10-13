{
    "title": "Tags",
    "sidebar": true,
    "weight": "1"
}



{{ $tags := .Params.tags }}
<ul>
{{ range $key, $taxonomy := .Site.Taxonomies.tags }}
  {{ if eq $key $tags }}
    {{ range $taxonomy.Pages }}
    <li><a href="{{ .Permalink }}">{{ .Title }}</a></li>
    {{ end }}
  {{ end }}
{{ end }}
</ul>

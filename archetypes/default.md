---
title: "{{ replace .Name "-" " " | title }}"
date: {{ .Date }}
draft: true
---








<ul>
    {{ range (.GetTerms "tags") }}
        <li><a href="{{ .Permalink }}">{{ .LinkTitle }}</a></li>
    {{ end }}
</ul>

** Categories: **
<br/>
<ul>
{{ range .Site.RegularPages }}
    <li>   
    Title: {{ .Title }} - Categories:
    {{ range .Params.categories }}{{ . }}{{ end }}
    </li>
{{ end }}
</ul>

---
title: render
# linktitle: Render
description: Takes a view to apply when rendering content.
godocref:
date: 2017-02-01
publishdate: 2017-02-01
lastmod: 2017-02-01
categories: [functions]
menu:
  docs:
    parent: "functions"
#tags: [views]
signature: ["render LAYOUT"]
workson: []
hugoversion:
relatedfuncs: []
deprecated: false
aliases: []
---

The view is an alternative layout and should be a file name that points to a template in one of the locations specified in the documentation for [Content Views](/templates/views).

This function is only available when applied to a single piece of content within a [list context][].

This example could render a piece of content using the content view located at `/layouts/_default/summary.html`:

```golang
{{ range .Data.Pages }}
    {{ .Render "summary"}}
{{ end }}
```

[list context]: /templates/lists/

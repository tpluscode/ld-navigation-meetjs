# Routing is brittle

Given a route like:

```
/person/{id}
```

Why extract parameters and build API URLs?

``` js
var url = "http://my.api/data/person/" + route.params.id;
```

1. What if the pattern changes?
1. What if you need multiple patterns for a resource type?
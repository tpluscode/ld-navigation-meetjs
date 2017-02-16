# Views are also brittle

View is chosen based on route and not data

``` html
<!-- React -->
<Route path="users" component={Users} />
```

``` js
// ui-router for Anuglar 2
let aboutState = { name: 'about', url: '/about',  component: About };
```

```
// Elm
render model =
  case model.route of
    HomeRoute ->
      h1 [] [ text "Home" ]
```
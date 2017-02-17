# Solution: `<ld-navigator>`

Turns the browser address into `apiUrl` and handles browser history.

Let your code handle choose the view depending on the actual data.

``` html
<ld-navigator resource-url="{{apiUrl}}" base="http://localhost:8000/data"></ld-navigator>

<iron-ajax auto url="[[apiUrl]]" last-response="{{data}}" handle-as="json"></iron-ajax>

<iron-pages attr-for-selected="id" selected="[[data._type]]" fallback-selection="Index">
    <div id="Index"></div>
    <div id="Slide">
        <ld-link resource-url="{{data.linkedResource}}">
        </ld-link>
    </div>
    <!-- etc. -->
</iron-pages>
```
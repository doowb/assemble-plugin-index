The following listing shows an example `index` template:

```html
<ul>
  {{#each items}}
    <li><a href="{{url}}">{{title}}</a></li>
  {{/each}}
</ul>
{{#with pagination}}
  <ul>
    {{#if isFirst}}
      <li><a>Prev</a></li>
    {{else}}
      <li><a href="{{prev}}">Prev</a></li>
    {{/if}}
    {{#each pages}}
      {{#is this ../current}}
        <li><a>{{@index}}</a></li>
      {{else}}
        <li><a href="{{this}}">{{@index}}</a></li>
      {{/is}}
    {{/each}}
    {{#if isLast}}
      <li><a>Next</a></li>
    {{else}}
      <li><a href="{{last}}">Next</a></li>
    {{/if}}
  </ul>
{{/with}}
```

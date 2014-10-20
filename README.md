# ember-radio-button

This is an ember-cli addon for an Ember `radio-button` component.

It allows a group of radio buttons with different `value` values
to bind to a single property called `groupValue`. Clicking on the component will set
`groupValue` to the value of `value`. The radio button will be in a checked state
when `groupValue === value`.

The component also exposes a `changed` action that allows you to do something
when clicking one of your radio buttons results in the value changing. This is useful
if you want to autosave a model in response to a user action, rather than with an observer.

Handlebars:
```javascript
{{#radio-button value="green" groupValue=color changed="colorChanged"}}
  Green
{{/radio-button}}
{{#radio-button value="blue" groupValue=color changed="colorChanged"}}
  Blue
{{/radio-button}}
```

Results in:
```html
<span id="ember336" class="ember-view radio-button">
  <label>
    <input id="ember345" class="ember-view" type="radio" value="green">
    Green
  </label>
</span>
<span id="ember347" class="ember-view radio-button checked">
  <label>
    <input id="ember348" class="ember-view" type="radio" value="blue">
    Blue
  </label>
</span>
```

This README outlines the details of collaborating on this Ember addon.

## Installation

* `git clone` this repository
* `npm install`
* `bower install`

## Running

* `ember server`
* Visit your app at http://localhost:4200.

## Running Tests

* `ember test`
* `ember test --server`

## Building

* `ember build`

For more information on using ember-cli, visit [http://www.ember-cli.com/](http://www.ember-cli.com/).

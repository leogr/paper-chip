`paper-chip`
===========

Material design: [Chips](https://material.io/guidelines/components/chips.html#).

> Polymer 2.x `<paper-chip>` may contain a icon or a photo, some line of text or a contact information with Material Design styling.

## Usage

Basic paper-chip
```html
<paper-chip single-line>
    <div slot="label" class="label">Single-line Chip</div>
</paper-chip>
```

It can show **single-line** or **multi-line** text. You can open a multi-line chip tapping on it.
```html
<paper-chip>
    <iron-icon slot="icon" class="icon" icon="avatars:avatar-1"></iron-icon>
    <div slot="label" class="label">John Foo</div>
    <div slot="caption" class="caption">jfoo@doh.com</div>
</paper-chip>
```

Configure some basic behavior. It may be removable or not.

```html
<paper-chip removable>
    <div slot="label" class="label">Removable Chip</div>
</paper-chip>
```

Choose to set animation in openable chip.

```html
<paper-chip removable animated>
    <div slot="icon" class="icon">P</div>
    <div slot="label" class="label">John Foo</div>
    <div slot="caption" class="caption">jfoo@doh.com</div>
</paper-chip>
```

Use `<paper-chip-input>` component to collect a set of `chip`

```html
    <paper-chip-input></paper-chip-input>
```

Use `<paper-chip-input-autocomplete>` when you have a preset input values

```html
    <paper-chip-input-autocomplete></paper-chip-input-autocomplete>
```
You can load input values with `datasource` property.

The default properties for datasource are `label` and `value`, but you can configure it from outside by the properties `display-property` and `value-property`.

```html
<paper-chip-input-autocomplete display-property="value" value-property="key">
</paper-chip-input-autocomplete>
```
```json
{ "value": "apple", "key": 0 },
{ "value": "apricot", "key": 1 }
```

## Styling
The following custom properties and mixins are available for styling:

Custom property | Description | Default
----------------|-------------|----------
`--paper-chip-secondary-text-color` | The paper-chip label-color |
`--paper-chip-background-color` | The paper-chip background-color |
`--paper-chip-icon-background-color` | The paper-chip avatar background-color |
`--paper-chip-icon-text-color` | The paper-chip icon color |

## Testing
If you are using **polyserve** navigate to the `test/` directory of your element to run its tests. You can view results in browser console.

### web-component-tester

The tests are compatible with [web-component-tester](https://github.com/Polymer/web-component-tester).

Install it via:

```sh
npm install web-component-tester
```

The `wct` tool will run your tests in all the browsers you have installed. Just
run it:

```sh
wct
```

By default, any tests under `test/` will be run. You can override this by
specifying particular files (or globs of files) via `wct path/to/files`.

Otherwise you can run the test suite via npm script

```sh
npm test
```

## License
MIT © fabbricadigitale




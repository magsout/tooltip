# Tooltip

> Simple tooltip using an html attribute for the content

## Usage

Example:

```html
<span class="rcp-Tooltip rcp-Tooltip--bottom" data-rcp-tooltip="I'm the tooltip body">Hover me to see the tooltip !</span>
```

## Available classes

### `.rcp-Tooltip`

#### Position modifiers

##### `.rcp-Tooltip--top`
##### `.rcp-Tooltip--bottom`
##### `.rcp-Tooltip--left`
##### `.rcp-Tooltip--right`

#### Visibility modifier

##### `.rcp-Tooltip--visible`

## Availables custom properties

```css
:root {
	--rcp-Tooltip-zIndex: 1000;
	--rcp-Tooltip-backgroundColor: #383838;
	--rcp-Tooltip-margin: .5rem;

	--rcp-Tooltip-arrow-size: .5rem;
}
```

## Customize

If custom properties are not enough, you can obviously override default rules. Or add modifier(s).

### Adding a state

It's easy to add a `success` or `error` state.

```css
.rcp-Tooltip--STATE::after {
	background-color: var(--rcp-Tooltip--STATE-color);
	text-shadow: 0 -1px 0 color(var(--rcp-Tooltip--STATE-color) blackness(90%));
}
	.rcp-Tooltip--STATE.rcp-Tooltip--top::before { border-top-color: var(--rcp-Tooltip--STATE-color) }
	.rcp-Tooltip--STATE.rcp-Tooltip--bottom::before { border-bottom-color: var(--rcp-Tooltip--STATE-color) }
	.rcp-Tooltip--STATE.rcp-Tooltip--left::before { border-left-color: var(--rcp-Tooltip--STATE-color) }
	.rcp-Tooltip--STATE.rcp-Tooltip--right::before { border-right-color: var(--rcp-Tooltip--STATE-color) }
```

## Testing

_Requires [nodejs](http://nodejs.org)_

To generate a build:

	npm run build

To generate the testing build.

	$ npm run build-test

Basic visual tests are in `test/index.html`.

## [Changelog](CHANGELOG.md)

## [License](LICENSE-MIT)
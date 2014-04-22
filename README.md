# WAI-ARIA Web Component

A simple example of how WAI-ARIA can be employed within web component designs. Uses Polymer to polfill.

## Basic usage

```
<disclosure-widget summary="Some info">
  <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Etiam pellentesque lectus at convallis placerat. Curabitur et nunc est. Sed non consequat dolor, nec consequat risus. In auctor, lacus vel ultricies pulvinar, nulla augue interdum velit, nec imperdiet risus eros vitae ligula.</p>
</disclosure-widget>
```

## Open by default (using the supplied `open` attribute)

```
<disclosure-widget summary="More info" open>
  <p>Duis sagittis lacus lacus, eu iaculis nulla fermentum non. Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas. Etiam tempus erat risus, sit amet molestie arcu commodo non. Suspendisse tincidunt sem vitae erat aliquam ornare.</p>
</disclosure-widget>
```

## What the generated (Shadow) DOM looks like

```
<disclosure-widget summary="Some info">
	<div role="group">
		<button on-click="{{ toggleContent }}" aria-expanded="false">Some info</button>
		<div tabindex="0" aria-hidden="true">
			<p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Etiam pellentesque lectus at convallis placerat. Curabitur et nunc est. Sed non consequat dolor, nec consequat risus. In auctor, lacus vel ultricies pulvinar, nulla augue interdum velit, nec imperdiet risus eros vitae ligula.</p>
		</div>
	</div>
</disclosure-widget>
```

## Demo page

I host the demo page on my own domain: [http://www.heydonworks.com/accessible-web-component-with-aria/](http://www.heydonworks.com/accessible-web-component-with-aria/)
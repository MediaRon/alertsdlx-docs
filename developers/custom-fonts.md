# Custom Fonts

This section covers how to disable the AlertsDLX Lato font for performance and specify your own fonts for AlertsDLX to use.

### Disable the Lato Font Using Filter: `alerts_dlx_load_fonts`

Use the following code snippet to disable the Lato font. This should improve performance and prevent loading the Lato font files.

```php
/**
 * This disables the AlertsDLX Fonts.
 */
add_filter( 'alerts_dlx_load_fonts', '__return_false' );
```

### Use an Alternate Font Using Filter: `alerts_dlx_default_font_family`

Use the following to load an alternate font, for example, a font from your theme.

```php
<?php
/**
 * AlertsDLX Disable Fonts
 *
 * @package AlertsDLX
 * @subpackage Fonts
 * @since 2.3.0
 */

/**
 * This disables the AlertsDLX Fonts.
 */
add_filter( 'alerts_dlx_load_fonts', '__return_false' );

/**
 * This changes the default font family to Raleway.
 *
 * @return string The default font family.
 */
add_filter(
	'alerts_dlx_default_font_family',
	function () {
		return 'Raleway, sans-serif';
	}
);
```

For a full list of available filters, see [Filters and Hooks](filters-and-hooks.md).

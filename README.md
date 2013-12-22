dashicons-picker
================

A jQuery plugin to make picking [Dashicons](http://melchoyce.github.io/dashicons/) in WordPress a breeze

![dashicons-picker](https://raw.github.com/bradvin/dashicons-picker/master/dashicons-picker-jquery-plugin.jpg "dashicons-picker")

## Installation ##

First, include both the dashicons-picker.css and dashicons-picker.js files:

```
function dashicons_picker_scripts() {
	$css = plugin_dir_url( __FILE__ ) . 'css/dashicons-picker.css';
    wp_enqueue_style( 'dashicons-picker', $css, array( 'dashicons' ), '1.0' );

	$js = plugin_dir_url( __FILE__ ) . 'js/dashicons-picker.js';
	wp_enqueue_script( 'dashicons-picker', $js, array( 'jquery' ), '1.0' );
}
add_action( 'admin_enqueue_scripts', 'dashicons_picker_scripts' );</pre>
```

Together, the 2 files are less than 8KB. And that is unminified, which is very small indeed. And as you can see in the code above, the CSS file is dependent on 'dashicons' so that will automatically include the stylesheets needed to view the dashicons font.

Then in your HTML, give the button a class or "dashicons-picker" and include a data-target attribute which stores the selector to the textbox:

```
<input class="regular-text" id="dashicons_picker_example_icon1" type="text" />
<input class="button dashicons-picker" type="button" value="Choose Icon" data-target="#dashicons_picker_example_icon1" />
```

## Plugin Example ##
Download this [entire repo](https://github.com/bradvin/dashicons-picker/archive/master.zip) as a zip, and install it like you would any other plugin. A new settings page called "Dashicons Picker Example" will be available where you can play with the icon picker.

## Thanks ##

Thanks to these projects for inspiration, ideas and code:

* [http://victor-valencia.github.io/bootstrap-iconpicker/](http://victor-valencia.github.io/bootstrap-iconpicker/)
* [http://titosust.github.io/Bootstrap-icon-picker/](http://titosust.github.io/Bootstrap-icon-picker/)
=== Plugin Name ===
Contributors: bfintal
Donate link: https://www.paypal.com/cgi-bin/webscr?cmd=_s-xclick&hosted_button_id=D2MK28E7BDLHC
Tags: framework, options, admin, admin panel, meta box, theme customizer, option framework, library, sdk
Requires at least: 3.8
Tested up to: 3.8.1
Stable tag: 1.0
License: GPLv2 or later
License URI: http://www.gnu.org/licenses/gpl-2.0.html

The most easy to use WordPress option framework.

== Description ==

Titan Framework allows theme and plugin developers to create a admin pages, options, meta boxes, and theme customizer options with just a few simple lines of code.

**For developers: for documentation and examples, please visit our website at [titanframework.net](http://titanframework.net)**

= Features =

* Makes development unbelievably easy
* Built with optimization in mind
* Does NOT clutter the database
* Integrates with your project seamlessly
* Theme customizer live preview integration

= Easy creation of: =

* Admin menus and submenus
* Admin pages
* Admin options and tabs
* Meta boxes and options
* Theme customizer sections and options

= Options available in admin pages, meta boxes and theme customizer: =

* Checkbox
* Color picker
* Heading
* Media uploader
* Multicheck
* Multicheck categories and taxonomies
* Multicheck pages and posts
* Note
* Number
* Radio buttons
* Save and reset buttons
* Select (drop down)
* Select Google WebFont
* Select categories and taxonomies
* Select pages and posts
* Text
* Textarea

**For developers: for documentation and examples, please visit our website at [titanframework.net](http://titanframework.net)**

== Installation ==

1. Upload `plugin-name.php` to the `/wp-content/plugins/` directory
2. Activate the plugin through the 'Plugins' menu in WordPress
3. Use the provided classes and functions in your theme or plugin

== Frequently Asked Questions ==

**Please visit our website at [titanframework.net](http://titanframework.net)**

== Sample Code ==

= Creating an admin menu and submenu =

`$titan = TitanFramework::getInstance( 'my-plugin' );

// Create menu
$panel = $titan->createAdminPanel( array(
    'name' => 'Menu Name',
) );

$panel2 = $panel->createAdminPanel( array(
    'name' => 'Submenu Name',
) );`

= Creating an option in an admin page =

`$titan = TitanFramework::getInstance( 'my-plugin' );

// Create menu
$panel = $titan->createAdminPanel( array(
    'name' => 'Menu Name',
) );

// Create a select option
$panel->createOption( array(
    'name' => 'Select One',
    'id' => 'my_selected_id
    'type' => 'select',
    'options' => array(
        '1' => 'Option one',
        '2' => 'Option two',
        '3' => 'Option three',
    ),
    'default' => '3',
    'desc' => 'Some description',
) );`

= Create a meta box with an option =

`$titan = TitanFramework::getInstance( 'my-plugin' );

// Create menu
$box = $titan->createMetaBox( array(
    'name' => 'Menu Name',
) );

$box->createOption( array(
    'name' => 'My Text',
    'type' => 'text',
    'id' => 'my_text_id',
    'desc' => 'Some description',
) );`

= Create a theme customizer with an option with live preview =

`$titan = TitanFramework::getInstance( 'my-plugin' );

$section = $titan->createThemeCustomizerSection( array(
    'name' => 'My Section',
    'desc' => 'Section description',
) );

$section->createOption( array(
    'id' => 'my_color',
    'name' => 'My Color',
    'type' => 'color',
    'default' => '#555555',
    'livepreview' => "$('#main').css('backgroundColor', value);",
) );`

= Getting values =

`$titan = TitanFramework::getInstance( 'my-plugin' );

// Get an option or an admin option
$myValue = $titan->getOption( 'option_name' );

// Get a theme customizer option
$myValue = $titan->getOption( 'option_name', $post_id );`

**For developers: for documentation and examples, please visit our website at [titanframework.net](http://titanframework.net)**

== Changelog ==

= 1.0 =
First release
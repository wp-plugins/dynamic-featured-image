=== Dynamic Featured Image ===
Contributors: ankitpokhrel
Donate link: https://www.paypal.com/cgi-bin/webscr?cmd=_s-xclick&hosted_button_id=J9FVY3ESPPD58
Tags: dynamic featured image, featured image, post thumbnail, dynamic post thumbnail, multiple featured image, multiple post thumbnail
Requires at least: 3.3
Tested up to: 3.6.1
Stable tag: 1.1.2
License: GPLv2 or later
License URI: http://www.gnu.org/licenses/gpl-2.0.html

Dynamically adds multiple featured image (post thumbnail) functionality to posts, pages and custom post types.

== Description ==
Dynamically add multiple featured image or post thumbnail functionality to your page, posts and custom post types. This plugin is unique from other
wordpress featured image plugin because there is no need to add code in functions.php file for every featured image. 

**Overview**

Dynamic Featured Image enables the option to have MULTIPLE featured images within a post or page. 
This is especially helpful when you use other plugins, post thumbnails or sliders that use featured images. 
Why limit yourself to only one featured image if you can do some awesome stuffs with multiple featured image? 
DFI allows you to add different number of featured images to each post and page that can be collected by the various theme functions.

**How it works?**

1. After successfull plugin activation go to `add` or `edit` page of posts or pages and you will notice a box for second featured image.
2. Click `Set featured image`, select required image from media popup and click `Insert into Post`.
3. Click on `Add New` to add new featured image or use `Remove` link to remove the featured image box.
4. You can then get the images by calling the function  `dfiGetFeaturedImages([$postId (optional)])` in your theme.
5. The data will be returned in the following format.
`
array
  0 => 
    array
      'thumb' => string 'http://your_site/upload_path/yourSelectedImage.jpg' (length=50)
      'full' => string 'http://your_site/upload_path/yourSelectedImage_fullSize.jpg' (length=69)
  1 => 
    array
      'thumb' => string 'http://your_site/upload_path/yourSelectedImage.jpg' (length=50)
      'full' => string 'http://your_site/upload_path/yourSelectedImage_fullSize.jpg' (length=69)
  2 => ...
`

**Extended Documentation**

[Click here](https://github.com/ankitpokhrel/Dynamic-Featured-Image "Click here for documentation") for detail documentation.

**Contribute**

If you'd like to check out the code and contribute, join us on [Github](https://github.com/ankitpokhrel/Dynamic-Featured-Image "View this plugin in github"). 
Pull requests, issues, and plugin recommendations are more than welcome!

== Installation ==

1. Unzip and upload the `dynamic-featured-images` directory to the plugin directory (`/wp-content/plugins/`) or install it from `Plugins->Add New->Upload`.
2. Activate the plugin through the `Plugins` menu in WordPress.
3. If you don't see new featured image box, click `Screen Options` in the upper right corner of your wordpress admin and make sure that the `Featured Image 2` box is slected.

== Frequently Asked Questions ==
= 1. The media uploader screen freezes and stays blank after clicking insert into post? =
The problem is usually due to the conflicts with other plugin or theme. You can use general debugging technique to find out the problem.

1. Switch to the default wordpress theme to rule out any theme-specific problems.
2. Try the plugin in a fresh new WordPress installation.
3. If it works, deactivate all plugins from your current wordpress installation to see if this resolves the problem. If this works, re-activate the plugins one by one until you find the problematic plugin(s).
4. [Resetting the plugins folder](http://www.google.com/url?q=http%3A%2F%2Fcodex.wordpress.org%2FFAQ_Troubleshooting%23How_to_deactivate_all_plugins_when_not_able_to_access_the_administrative_menus.3F&sa=D&sntz=1&usg=AFQjCNFaei9nyiMZe2yZQUBBA_MghJ-Wxw) by FTP or PhpMyAdmin. Sometimes, an apparently inactive plugin can still cause problems.

= Other problems or questions? =
You can always contact me at `ankitpokhrel@gmail.com`, if you have any question or queries about the project. 
I am available for freelance work too.

Please feel free to report any bug found at https://github.com/ankitpokhrel/Dynamic-Featured-Image/ or `ankitpokhrel@gmail.com`.

== Screenshots == 
1. New featured image box.
2. Selecting image from media box.
3. Add new featured image box.

== Changelog ==
= 1.1.2 =
* Resolved media uploader conflicts.

= 1.1.1 =
* Fixed a bug on user access for edit operation.

= 1.1.0 =
* Major security update
* Now uses AJAX to create new featured box
 
= 1.0.3 =
* First stable version with minimum features released.
* Fixed bug for duplicate id.
* Updated dfiGetFeaturedImages function to accept post id.
* Fixed some minor issues.
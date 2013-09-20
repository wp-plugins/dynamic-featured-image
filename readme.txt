=== Dynamic Featured Image ===
Contributors: ankitpokhrel
Donate link: http://ankitpokhrel.com.np/
Tags: dynamic featured image, featured image, post thumbnail, dynamic post thumbnail, multiple featured image, multiple post thumbnail
Requires at least: 3.3
Tested up to: 3.6.1
Stable tag: 1.0.3
License: GPLv2 or later
License URI: http://www.gnu.org/licenses/gpl-2.0.html

Dynamically adds multiple featured image (post thumbnail) functionality to posts, pages and custom post types.

== Description ==
Dynamically add multiple featured image or post thumbnail functionality to your page, posts and custom post types. This plugin is unique from other
wordpress featured image plugin because there is no need to add code in functions.php file for every featured image. You can contribute to this plugin
at [Github](https://github.com/ankitpokhrel/Dynamic-Featured-Image "View this plugin in github")

== How it works? ==

1. After successfull plugin activation go to `add` or `edit` page of posts or pages and you will notice a box for second featured image.

   ![Snapshot 1](http://ankitpokhrel.com.np/dfi/snapshot_1.jpg)

2. Click `Set featured image`, select required image from media popup and click `Insert into Post`.

   ![Snapshot 2](http://ankitpokhrel.com.np/dfi/snapshot_2.jpg)

3. Click on `Add New` to add new featured image or use `Remove` link to remove the featured image box.
 
   ![Snapshot 3](http://ankitpokhrel.com.np/dfi/snapshot_3.jpg)

4. After adding featured images click `publish` or `update` to save featured images.

###### _Note: The featured images are only saved when you publish or update the post._


== Retrieving Images in a Theme ==

* To get featured images of specific post

`
if( function_exists('dfiGetFeaturedImages') )
   $featuredImages = dfiGetFeaturedImages($postId);
`

* To get featured images in a post loop.

`
<?php 
   while ( have_posts() ) : the_post();

   if( function_exists('dfiGetFeaturedImages') ) {
       $featuredImages = dfiGetFeaturedImages();
   }
   
   endwhile;
?>
`

* The data is returned as an array that contain selected image and full size path to the selected image.

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

== Installation ==

 1. Unzip and upload the dynamic-featured-images directory to the plugin directory (/wp-content/plugins/) or install it from Plugins->Add New->Upload.
 2. Activate the plugin through the Plugins menu in WordPress.

== Frequently Asked Questions ==

You can always contact me at `ankitpokhrel@gmail.com`, if you have any question or queries about the project. 
I am available for freelance work too.

Please feel free to report any bug found at https://github.com/ankitpokhrel/Dynamic-Featured-Image/ or `ankitpokhrel@gmail.com`.

 == Screenshots == 

 == Changelog == 
 = 1.0.3 =
* First stable version with minimum features released.
* Fixed bug for duplicate id.
* Updated dfiGetFeaturedImages function to accept post id.
* Fixed some minor issues.
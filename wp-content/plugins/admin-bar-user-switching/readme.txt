=== Admin Bar User Switching ===
Contributors: wpmarkuk
Donate link: http://markwilkinson.me/saythanks/
Tags: users, user switching
Requires at least: 3.1
Tested up to: 4.0.1
Stable tag: 1.0.6
License: GPLv2 or later
License URI: http://www.gnu.org/licenses/gpl-2.0.html

Extends the excellent User Switching plugin by John Blackbourn by adding a User Switching to the admin bar for quick and easy user switching.

== Description ==

An admin bar “Switch to User” option is provided which on hover provides a search box where you can query a user to switch to. The results are links to switch to that user. This plugin is great for when you are building sites for clients and it is beneficial to see the site as your logged in client see's it.

== Installation ==

To install the plugin:

1. Upload to the `/wp-content/plugins/` directory
2. Activate the plugin through the 'Plugins' menu in WordPress

== Frequently Asked Questions ==

**How do I switch to a user?**

As with the User Switching plugin you can still use the "Switch To" link on the users overview page - nothing changes there. However the point of this plugin is that it gives you a Switch to User link in the WordPress admin bar. This reveals a search box where you can search for a users username. The results of this search are clickable to "Switch To" that user.

**What can be entered into the username search box?**

You can enter the exact username of a user or you can use wildcards to find a user e.g. *another* would find all users with the word another in their username. [See here for more information on wildcard searches](http://codex.wordpress.org/Class_Reference/WP_User_Query#Search_Parameters). Clicking submit with nothing in the search box will search all users except the current logged in user.

**Has the plugin any filters or actions for developers?**

It does indeed, although not too many! The following filters can be used.

* abus_switch_to_text - allows developers to change the text that is displayed in the admin menu which, when on hover shows the search box
* abus_form_output - this filter can be used to change the markup of the form which is used in the plugin for user searching
* abus_switch_back_text - this filter is used to change the text shown to switch back to the original logged in user
* abus_switch_to_url- this filter is used to alter the redirect url for different users as the filter is passed to switch to user user object

== Screenshots ==

1. A Switch to user item is added to the WordPress admin bar to allow you to search for a user to switch to.

== Changelog ==

= 1.0.6 =
* Make the capability (edit_users by default) needed to be able to switch to users be filterable.

= 1.0.5 =
* Escape instances of add_query_arg in accordance with https://make.wordpress.org/plugins/2015/04/20/fixing-add_query_arg-and-remove_query_arg-usage/

= 1.0.4 =
* Correct an issues which could result in a PHP error when the plugin is active and the User Switching plugin is not active.
* Add filter for the switch to redirect url named `abus_switch_to_url` - this allows devs to alter the redirect url for different users as the filter is passed to switch to user user object.

= 1.0.3 =
* Output styles on both front and backend to make the form look correct when results are returned.
* Create a filter for developers to amend the styles as needed to match their theme
* Use correct hook for enqueuing javascript file
* Make sure the current logged in user does not appear in the search results

= 1.0.2 =
* Thanks for @johnbillion for pointing out the incorrect capabilities check for switch_to_user. This now checks against edit_user so users who can edit users will be the Swtich to link.

= 1.0.1 =
* Use switch_to_user user capability instead of is_super_admin when checking whether to display Switch to link in admin bar.

= 1.0 =
* Make the Switch to User link reveals a user search box
* Uses AJAX to populate the user switch to list which therefore makes the plugin more compatible for sites with lots of users.

= 0.1 =
* Initial release.

== Upgrade Notice ==
Update through the WordPress admin as notified.

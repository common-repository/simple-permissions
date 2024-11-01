=== Plugin Name ===
Contributors: george_michael
Donate link: 
Tags: 
Requires at least: 3.5.2
Tested up to: 4.4.2
Stable tag: 1.2.4
License: GPLv2 or later
License URI: http://www.gnu.org/licenses/gpl-2.0.html

Create simple permission groups for reading or editing posts.

== Description ==

If you just want a simple plugin that lets you create groups and limit posts or pages (and probably custom types, though that's untested!) to be read or edited by only those groups, then this is the plugin for you.

This plugin checks a users group membership when getting posts, so if a user isn't a member of a group and that group is the only group that can read the post, the user won't see it in a list view (admin or regular) or a direct link.

There are exceptions, of course. If a user is a member of a group that has the write permission to a post, but that user does not have a WP role that allows for editing that document (a subscriber, for instance), they won't be able to edit it. Also, authors and admins are not group limited. If you wrote it, you can edit it. If you're an admin, you can edit it.

== Installation ==

1. Upload `simple-permissions.php` to the `/wp-content/plugins/` directory
1. Activate the plugin through the 'Plugins' menu in WordPress

== Frequently Asked Questions ==


== Screenshots ==

1. The main settings page with group list.
2. The settings when editing a group.
3. The permissions settings meta box when editing a post.

== Changelog ==

= 1.2.4 =
* Fixed some javascript handling checkboxes on the edit meta box.
* Fixed an issue where superadmins could not view protected posts.

= 1.2.2 =
* Removed PHP4 constructor from class as WP 4.3 deprecated that type of constructor.

= 1.2.1 =
* Changed so that an author will always have the ability to edit their own post. If you don't want an author to have access, you should change the ownership of the post.

= 1.2.0 =
* Fixed (hopefully!) an issue where you would not be redirected to the proper page after login when presented with a protected page notice. I'm getting around this by not redirecting at all. Instead, I'm replacing the requested pages content with the content of the protected page notice.

= 1.1.4 =
* Bug fix that was preventing drafts from autosaving.

= 1.1.3 =
* Removing category limits was not working under all conditions. Should be fixed now.

= 1.1.2 =
* Fixed a bug that would cause Wiki plugin (and anything else that provides an editing interface) to reset permissions on posts.

= 1.1.1 =
* Quick bug fix for major oops in last version. The meta box wasn't rendering if a user had a higher role than necessary.

= 1.1.0 =
* Added option to limit changing permissions to certain WP roles.
* Added ability to prevent posting in categories by SP group.
* Changed the regular express used to find usernames when added users to a group. This will allow spaces in usernames, though WP may have to be changed to allow it.
* above changes per http://wordpress.org/support/topic/couple-issues-3

= 1.0.2 =
* Fixed big bug that prevented editing of posts that had no permissions set.

= 1.0.1 =
* Fixed issue with some extra whitespace killing feeds

= 1.0.0 =
* Initial version.

== Upgrade Notice ==

= 1.2.4 =
* Bug fixes. Upgrade recommended.

= 1.2.2 =
* Required upgrade if using WP 4.3.

= 1.2.1 =
* Changed permission logic. Upgrade suggested.

= 1.2.0 =
* Pretty significant bug fix. Upgrade suggested.

= 1.1.4 =
* Minor bug fix. Upgrade if you were having trouble auto saving drafts.

= 1.1.3 =
* Everyone should update as some functionality wasn't working.

= 1.1.2 =
* Bug fix for interaction with Wiki plugin. Upgrade optional.

= 1.1.1 =
* Bug fix for 1.1.0, so if you had 1.1.0, you need to upgrade. If on 1.0.2, upgrade is optional.

= 1.1.0 =
* New features and options based on feedback. Upgrade optional.

= 1.0.2 =
* Everyone should update.
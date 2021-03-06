=== WP Discourse ===
Contributors: cdck, retlehs, samsaffron, scossar, techapj
Tags: discourse, forum, comments, sso
Requires at least: 4.4
Tested up to: 4.6
Stable tag: 0.9.7
License: GPLv2 or later
License URI: http://www.gnu.org/licenses/gpl-2.0.html

This plugin allows you to use Discourse as a community engine for your WordPress website.

== Description ==

The WP Discourse plugin acts as an interface between your WordPress site and your
[Discourse](http://www.discourse.org/) forum.

It allows you to:

- Publish WordPress posts to Discourse
- Use Discourse to generate comments and discussion for your WordPress posts
- Select which comments are to be displayed on the WordPress site based on post score and commenter trust level
- Use your WordPress site as the Single Sign On provider for your Discourse forum

#### See it live

- [blog.discourse.org](http://blog.discourse.org/)
- [boingboing.net](http://boingboing.net/)
- [howtogeek.com](http://www.howtogeek.com/)
- [talkingpointsmemo.com](http://talkingpointsmemo.com/)

== Installation ==

#### From your WordPress dashboard

1. Visit 'Plugins > Add New'
2. Search for 'WP Discourse'
3. Activate WP Discourse from your Plugins page

#### From wordpress.org

1. Download WP Discourse
2. Upload the 'wp-discourse' directory to your '/wp-content/plugins/' directory
3. Activate WP Discourse from your Plugins page

For more detailed instructions please see the [setup](https://github.com/discourse/wp-discourse/wiki/Setup) page of the
[wp-discourse wiki](https://github.com/discourse/wp-discourse/wiki)

== Frequently Asked Questions ==

= Does this plugin install Discourse for me? =

No this plugin acts as an interface between Discourse and WordPress. For it to work you will need to first set up
Discourse forum. You can install Discourse for yourself following either of these guides:

- [Install Discourse in Under 30 Minutes](https://github.com/discourse/discourse/blob/master/docs/INSTALL-cloud.md)
- [How to use the Discourse One-Click Application on DigitalOcean](https://www.digitalocean.com/community/tutorials/how-to-use-the-discourse-one-click-application-on-digitalocean)

= Is it possible to customize the comment templates? =

Yes, the html templates used for publishing posts on Discourse and for displaying comments on WordPress can be customized in your theme.
This is done by hooking into the filters that are applied to each template.

For more details on template customization, take a look at this section of our wiki: [Template Customization](https://github.com/discourse/wp-discourse/wiki/Template-Customization)

== Screenshots ==

1. Select whether a post is to be published to Discourse, and what category it is to be published into.

2. A WordPress posts with no comments.

3. Adding a comment on the Discourse forum.

4. The comment appears on WordPress.


== Changelog ==


**note:** Have you made changes to the HTML templates? The template changes are no longer handled from the plugin
admin, They must be customized with filters. see the [Template Customization](https://github.com/discourse/wp-discourse/wiki/Template-Customization)
section of the [wiki](s://github.com/discourse/wp-discourse/wiki) for details.

#### 0.9.7 27/08/16

- Set expiration time on `sync_to_discourse` and `sync_comments` lock transients

#### 0.9.6 18/08/16

- Set `require_activation => 'true'` for SSO request after email address change on WordPress
- Sync logout from WordPress with Discourse

#### 0.9.5 16/08/16

- Require activation on Discourse when email address can't be verified by WordPress
- Tested up to WordPress 4.6

#### 0.9.4 16/08/10

- Fix: WordPress comment box showing when there are no WordPress comments

#### 0.9.3 16/07/21

- Fix: existing WordPress comments always showing
- Fix: youtube data attribute being escaped by wp_kses_post
- Substitute comment url for comment_url tag
- Internationalize comments_number function

#### 0.9.2 16/07/20

- Partial fix for emoji relative paths

#### 0.9.1 16/07/19

- Add option to redirect to Discourse without login
- Log error if validation filter is missing
- Check for post_types array before trying to access it

#### 0.9.0 16/07/18

- Verify email before logging into Discourse

#### 0.7.0 16/05/16

- Restructure code
- Move templates out of options
- Validate settings
- Add notices to indicate connection status
- Sanitize admin options page
- Sanitize comment template output
- Add type argument to text input method
- Use cached categories when there is a configuration error
- Fix name property not available in participants array
- Use `wp_get_current_user`
- Fix `add_query_arg` undefined offset notice
- Update Discourse post on WP post update
- Better method for including comments script
- Allow choosing Discourse category per post
- Replace avatar URL function
- Fix timezone for custom timestamp

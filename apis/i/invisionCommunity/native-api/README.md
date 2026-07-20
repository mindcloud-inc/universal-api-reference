# Invision Community: Native API Reference

A consolidated summary of Invision Community's API configuration and 116 documented operations, with links to official documentation.

- **Official docs:** https://invisioncommunity.com/developers/rest-api/index/
- **API base URL:** `{communityBaseUrl}/api`

## Authentication

### OAuth2

Connect an Invision Community tenant with OAuth2 authorization code.

### Credentials

- **Community Base URL:** `communityBaseUrl` · required · Your Invision Community root URL, for example https://your-community.example.com
- **Client ID:** `clientId` · required · The OAuth client identifier from your Invision Community tenant.
- **Client Secret:** `clientSecret` · required · The OAuth client secret from your Invision Community tenant.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to {{credentials.communityBaseUrl}}/oauth/authorize/ to approve access.
2. Exchange the returned authorization code with a POST request to {{credentials.communityBaseUrl}}/oauth/token/.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `profile`.

The flow supports refresh tokens. Refresh expired access tokens with a POST request to {{credentials.communityBaseUrl}}/oauth/token/.

[Official authentication documentation](https://invisioncommunity.com/developers/rest-api/index/)

## API conventions

Request bodies use URL-encoded form data.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/x-www-form-urlencoded` |

Responses from this API use JSON.

## Pagination

Use `perPage` in the query string to set the page size (default 25). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (116 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Applications](actions/get-applications.md) | `GET /core/applications` | [docs](https://invisioncommunity.com/developers/rest-api/index/) |
| [Get Blog](actions/get-blog.md) | `GET /blog/blogs/:id` | [docs](https://invisioncommunity.com/developers/rest-api/index/) |
| [Get Blog Category](actions/get-blog-category.md) | `GET /blog/categories/:id` | [docs](https://invisioncommunity.com/developers/rest-api/index/) |
| [Get Blog Comment](actions/get-blog-comment.md) | `GET /blog/comments/:id` | [docs](https://invisioncommunity.com/developers/rest-api/index/) |
| [Get Blog Entry](actions/get-blog-entry.md) | `GET /blog/entries/:id` | [docs](https://invisioncommunity.com/developers/rest-api/index/) |
| [Get Blog Entry Category](actions/get-blog-entry-category.md) | `GET /blog/entrycategories/:id` | [docs](https://invisioncommunity.com/developers/rest-api/index/) |
| [Get Calendar](actions/get-calendar.md) | `GET /calendar/calendars/:id` | [docs](https://invisioncommunity.com/developers/rest-api/index/) |
| [Get Calendar Comment](actions/get-calendar-comment.md) | `GET /calendar/comments/:id` | [docs](https://invisioncommunity.com/developers/rest-api/index/) |
| [Get Calendar Review](actions/get-calendar-review.md) | `GET /calendar/reviews/:id` | [docs](https://invisioncommunity.com/developers/rest-api/index/) |
| [Get Cloud Login Handler Member](actions/get-cloud-login-handler-member.md) | `GET /cloud/loginhandlers/:handler_id/member/:id` | [docs](https://invisioncommunity.com/developers/rest-api/index/) |
| [Get Club](actions/get-club.md) | `GET /core/clubs/:id` | [docs](https://invisioncommunity.com/developers/rest-api/index/) |
| [Get Club Member](actions/get-club-member.md) | `GET /core/clubs/:id/members/:member` | [docs](https://invisioncommunity.com/developers/rest-api/index/) |
| [Get CMS Category](actions/get-cms-category.md) | `GET /cms/databases/:database_id/:category_id` | [docs](https://invisioncommunity.com/developers/rest-api/index/) |
| [Get CMS Comment](actions/get-cms-comment.md) | `GET /cms/comments/:database_id/:id` | [docs](https://invisioncommunity.com/developers/rest-api/index/) |
| [Get CMS Database](actions/get-cms-database.md) | `GET /cms/databases/:id` | [docs](https://invisioncommunity.com/developers/rest-api/index/) |
| [Get CMS Record](actions/get-cms-record.md) | `GET /cms/records/:database_id/:record_id` | [docs](https://invisioncommunity.com/developers/rest-api/index/) |
| [Get CMS Review](actions/get-cms-review.md) | `GET /cms/reviews/:database_id/:id` | [docs](https://invisioncommunity.com/developers/rest-api/index/) |
| [Get Community Info](actions/get-community-info.md) | `GET /core/hello` | [docs](https://invisioncommunity.com/developers/rest-api?endpoint=core/hello/GETindex) |
| [Get Course](actions/get-course.md) | `GET /courses/courses/:id` | [docs](https://invisioncommunity.com/developers/rest-api/index/) |
| [Get Download Category](actions/get-download-category.md) | `GET /downloads/categories/:id` | [docs](https://invisioncommunity.com/developers/rest-api/index/) |
| [Get Download Comment](actions/get-download-comment.md) | `GET /downloads/comments/:id` | [docs](https://invisioncommunity.com/developers/rest-api/index/) |
| [Get Download File](actions/get-download-file.md) | `GET /downloads/files/:id` | [docs](https://invisioncommunity.com/developers/rest-api/index/) |
| [Get Download Review](actions/get-download-review.md) | `GET /downloads/reviews/:id` | [docs](https://invisioncommunity.com/developers/rest-api/index/) |
| [Get Event](actions/get-event.md) | `GET /calendar/events/:id` | [docs](https://invisioncommunity.com/developers/rest-api/index/) |
| [Get Event RSVP](actions/get-event-rsvp.md) | `GET /calendar/events/:id/rsvps/:member_id` | [docs](https://invisioncommunity.com/developers/rest-api/index/) |
| [Get Featured Content](actions/get-featured-content.md) | `GET /core/promotions/:id` | [docs](https://invisioncommunity.com/developers/rest-api/index/) |
| [Get Forum](actions/get-forum.md) | `GET /forums/forums/:id` | [docs](https://invisioncommunity.com/developers/rest-api/index/) |
| [Get Gallery Album](actions/get-gallery-album.md) | `GET /gallery/albums/:id` | [docs](https://invisioncommunity.com/developers/rest-api/index/) |
| [Get Gallery Category](actions/get-gallery-category.md) | `GET /gallery/categories/:id` | [docs](https://invisioncommunity.com/developers/rest-api/index/) |
| [Get Gallery Comment](actions/get-gallery-comment.md) | `GET /gallery/comments/:id` | [docs](https://invisioncommunity.com/developers/rest-api/index/) |
| [Get Gallery Review](actions/get-gallery-review.md) | `GET /gallery/reviews/:id` | [docs](https://invisioncommunity.com/developers/rest-api/index/) |
| [Get Group](actions/get-group.md) | `GET /core/groups/:id` | [docs](https://invisioncommunity.com/developers/rest-api/index/) |
| [Get Image](actions/get-image.md) | `GET /gallery/images/:id` | [docs](https://invisioncommunity.com/developers/rest-api/index/) |
| [Get Invoice](actions/get-invoice.md) | `GET /nexus/invoices/:id` | [docs](https://invisioncommunity.com/developers/rest-api/index/) |
| [Get License Key](actions/get-license-key.md) | `GET /nexus/lkey/:key` | [docs](https://invisioncommunity.com/developers/rest-api/index/) |
| [Get Member](actions/get-member.md) | `GET /core/members/:id` | [docs](https://invisioncommunity.com/developers/rest-api/index/) |
| [Get Member Follow](actions/get-member-follow.md) | `GET /core/members/:id/follows/:followKey` | [docs](https://invisioncommunity.com/developers/rest-api/index/) |
| [Get Member Warning](actions/get-member-warning.md) | `GET /core/members/:id/warning/:warning` | [docs](https://invisioncommunity.com/developers/rest-api/index/) |
| [Get Message](actions/get-message.md) | `GET /core/messages/:id` | [docs](https://invisioncommunity.com/developers/rest-api/index/) |
| [Get Message Reply](actions/get-message-reply.md) | `GET /core/messages/:id/reply/:replyId` | [docs](https://invisioncommunity.com/developers/rest-api/index/) |
| [Get My Email](actions/get-my-email.md) | `GET /core/me/email` | [docs](https://invisioncommunity.com/developers/rest-api/index/) |
| [Get My Profile](actions/get-my-profile.md) | `GET /core/me` | [docs](https://invisioncommunity.com/developers/rest-api/index/) |
| [Get Post](actions/get-post.md) | `GET /forums/posts/:id` | [docs](https://invisioncommunity.com/developers/rest-api/index/) |
| [Get Purchase](actions/get-purchase.md) | `GET /nexus/purchases/:id` | [docs](https://invisioncommunity.com/developers/rest-api/index/) |
| [Get Tag](actions/get-tag.md) | `GET /core/tags/:id` | [docs](https://invisioncommunity.com/developers/rest-api/index/) |
| [Get Topic](actions/get-topic.md) | `GET /forums/topics/:id` | [docs](https://invisioncommunity.com/developers/rest-api/index/) |
| [Get Transaction](actions/get-transaction.md) | `GET /nexus/transactions/:id` | [docs](https://invisioncommunity.com/developers/rest-api/index/) |
| [Get Venue](actions/get-venue.md) | `GET /calendar/venues/:id` | [docs](https://invisioncommunity.com/developers/rest-api/index/) |
| [Get Warn Reason](actions/get-warn-reason.md) | `GET /core/warnreasons/:id` | [docs](https://invisioncommunity.com/developers/rest-api/index/) |
| [Get Webhook](actions/get-webhook.md) | `GET /core/webhooks/:id` | [docs](https://invisioncommunity.com/developers/rest-api/index/) |
| [Get Withdrawal](actions/get-withdrawal.md) | `GET /nexus/withdrawals/:id` | [docs](https://invisioncommunity.com/developers/rest-api/index/) |
| [List Assignments](actions/list-assignments.md) | `GET /core/assignments` | [docs](https://invisioncommunity.com/developers/rest-api/index/) |
| [List Blog Categories](actions/list-blog-categories.md) | `GET /blog/categories` | [docs](https://invisioncommunity.com/developers/rest-api/index/) |
| [List Blog Comments](actions/list-blog-comments.md) | `GET /blog/comments` | [docs](https://invisioncommunity.com/developers/rest-api/index/) |
| [List Blog Entries](actions/list-blog-entries.md) | `GET /blog/entries` | [docs](https://invisioncommunity.com/developers/rest-api/index/) |
| [List Blog Entry Categories](actions/list-blog-entry-categories.md) | `GET /blog/entrycategories` | [docs](https://invisioncommunity.com/developers/rest-api/index/) |
| [List Blog Entry Comments](actions/list-blog-entry-comments.md) | `GET /blog/entries/:id/comments` | [docs](https://invisioncommunity.com/developers/rest-api/index/) |
| [List Blogs](actions/list-blogs.md) | `GET /blog/blogs` | [docs](https://invisioncommunity.com/developers/rest-api/index/) |
| [List Calendar Comments](actions/list-calendar-comments.md) | `GET /calendar/comments` | [docs](https://invisioncommunity.com/developers/rest-api/index/) |
| [List Calendar Reviews](actions/list-calendar-reviews.md) | `GET /calendar/reviews` | [docs](https://invisioncommunity.com/developers/rest-api/index/) |
| [List Calendars](actions/list-calendars.md) | `GET /calendar/calendars` | [docs](https://invisioncommunity.com/developers/rest-api/index/) |
| [List Club Content Types](actions/list-club-content-types.md) | `GET /core/clubs/contenttypes` | [docs](https://invisioncommunity.com/developers/rest-api/index/) |
| [List Club Members](actions/list-club-members.md) | `GET /core/clubs/:id/members` | [docs](https://invisioncommunity.com/developers/rest-api/index/) |
| [List Club Nodes](actions/list-club-nodes.md) | `GET /core/clubs/:id/nodes` | [docs](https://invisioncommunity.com/developers/rest-api/index/) |
| [List Clubs](actions/list-clubs.md) | `GET /core/clubs` | [docs](https://invisioncommunity.com/developers/rest-api/index/) |
| [List CMS Categories](actions/list-cms-categories.md) | `GET /cms/categories/:database_id` | [docs](https://invisioncommunity.com/developers/rest-api/index/) |
| [List CMS Comments](actions/list-cms-comments.md) | `GET /cms/comments/:database_id` | [docs](https://invisioncommunity.com/developers/rest-api/index/) |
| [List CMS Databases](actions/list-cms-databases.md) | `GET /cms/databases` | [docs](https://invisioncommunity.com/developers/rest-api/index/) |
| [List CMS Record Comments](actions/list-cms-record-comments.md) | `GET /cms/records/:database_id/:record_id/comments` | [docs](https://invisioncommunity.com/developers/rest-api/index/) |
| [List CMS Record Reviews](actions/list-cms-record-reviews.md) | `GET /cms/records/:database_id/:record_id/reviews` | [docs](https://invisioncommunity.com/developers/rest-api/index/) |
| [List CMS Records](actions/list-cms-records.md) | `GET /cms/records/:database_id` | [docs](https://invisioncommunity.com/developers/rest-api/index/) |
| [List CMS Reviews](actions/list-cms-reviews.md) | `GET /cms/reviews/:database_id` | [docs](https://invisioncommunity.com/developers/rest-api/index/) |
| [List Content Items](actions/list-content-items.md) | `GET /core/content` | [docs](https://invisioncommunity.com/developers/rest-api/index/) |
| [List Converters](actions/list-converters.md) | `GET /convert/converters` | [docs](https://invisioncommunity.com/developers/rest-api/index/) |
| [List Courses](actions/list-courses.md) | `GET /courses/courses` | [docs](https://invisioncommunity.com/developers/rest-api/index/) |
| [List Download Categories](actions/list-download-categories.md) | `GET /downloads/categories` | [docs](https://invisioncommunity.com/developers/rest-api/index/) |
| [List Download Comments](actions/list-download-comments.md) | `GET /downloads/comments` | [docs](https://invisioncommunity.com/developers/rest-api/index/) |
| [List Download File Comments](actions/list-download-file-comments.md) | `GET /downloads/files/:id/comments` | [docs](https://invisioncommunity.com/developers/rest-api/index/) |
| [List Download File History](actions/list-download-file-history.md) | `GET /downloads/files/:id/history` | [docs](https://invisioncommunity.com/developers/rest-api/index/) |
| [List Download File Reviews](actions/list-download-file-reviews.md) | `GET /downloads/files/:id/reviews` | [docs](https://invisioncommunity.com/developers/rest-api/index/) |
| [List Download Files](actions/list-download-files.md) | `GET /downloads/files` | [docs](https://invisioncommunity.com/developers/rest-api/index/) |
| [List Download Reviews](actions/list-download-reviews.md) | `GET /downloads/reviews` | [docs](https://invisioncommunity.com/developers/rest-api/index/) |
| [List Event Comments](actions/list-event-comments.md) | `GET /calendar/events/:id/comments` | [docs](https://invisioncommunity.com/developers/rest-api/index/) |
| [List Event Reviews](actions/list-event-reviews.md) | `GET /calendar/events/:id/reviews` | [docs](https://invisioncommunity.com/developers/rest-api/index/) |
| [List Event RSVPs](actions/list-event-rsvps.md) | `GET /calendar/events/:id/rsvps` | [docs](https://invisioncommunity.com/developers/rest-api/index/) |
| [List Events](actions/list-events.md) | `GET /calendar/events` | [docs](https://invisioncommunity.com/developers/rest-api/index/) |
| [List Featured Content](actions/list-featured-content.md) | `GET /core/promotions` | [docs](https://invisioncommunity.com/developers/rest-api/index/) |
| [List Forums](actions/list-forums.md) | `GET /forums/forums` | [docs](https://invisioncommunity.com/developers/rest-api/index/) |
| [List Gallery Albums](actions/list-gallery-albums.md) | `GET /gallery/albums` | [docs](https://invisioncommunity.com/developers/rest-api/index/) |
| [List Gallery Categories](actions/list-gallery-categories.md) | `GET /gallery/categories` | [docs](https://invisioncommunity.com/developers/rest-api/index/) |
| [List Gallery Comments](actions/list-gallery-comments.md) | `GET /gallery/comments` | [docs](https://invisioncommunity.com/developers/rest-api/index/) |
| [List Gallery Reviews](actions/list-gallery-reviews.md) | `GET /gallery/reviews` | [docs](https://invisioncommunity.com/developers/rest-api/index/) |
| [List Groups](actions/list-groups.md) | `GET /core/groups` | [docs](https://invisioncommunity.com/developers/rest-api/index/) |
| [List Image Comments](actions/list-image-comments.md) | `GET /gallery/images/:id/comments` | [docs](https://invisioncommunity.com/developers/rest-api/index/) |
| [List Image Reviews](actions/list-image-reviews.md) | `GET /gallery/images/:id/reviews` | [docs](https://invisioncommunity.com/developers/rest-api/index/) |
| [List Images](actions/list-images.md) | `GET /gallery/images` | [docs](https://invisioncommunity.com/developers/rest-api/index/) |
| [List Invoices](actions/list-invoices.md) | `GET /nexus/invoices` | [docs](https://invisioncommunity.com/developers/rest-api/index/) |
| [List Member Follows](actions/list-member-follows.md) | `GET /core/members/:id/follows` | [docs](https://invisioncommunity.com/developers/rest-api/index/) |
| [List Member Messages](actions/list-member-messages.md) | `GET /core/members/:id/messages` | [docs](https://invisioncommunity.com/developers/rest-api/index/) |
| [List Member Notifications](actions/list-member-notifications.md) | `GET /core/members/:id/notifications` | [docs](https://invisioncommunity.com/developers/rest-api/index/) |
| [List Member Warnings](actions/list-member-warnings.md) | `GET /core/members/:id/warnings` | [docs](https://invisioncommunity.com/developers/rest-api/index/) |
| [List Members](actions/list-members.md) | `GET /core/members` | [docs](https://invisioncommunity.com/developers/rest-api/index/) |
| [List Message Replies](actions/list-message-replies.md) | `GET /core/messages/:id/replies` | [docs](https://invisioncommunity.com/developers/rest-api/index/) |
| [List Messages](actions/list-messages.md) | `GET /core/messages` | [docs](https://invisioncommunity.com/developers/rest-api/index/) |
| [List Posts](actions/list-posts.md) | `GET /forums/posts` | [docs](https://invisioncommunity.com/developers/rest-api/index/) |
| [List Purchases](actions/list-purchases.md) | `GET /nexus/purchases` | [docs](https://invisioncommunity.com/developers/rest-api/index/) |
| [List Search Content Types](actions/list-search-content-types.md) | `GET /core/search/contenttypes` | [docs](https://invisioncommunity.com/developers/rest-api/index/) |
| [List Tags](actions/list-tags.md) | `GET /core/tags` | [docs](https://invisioncommunity.com/developers/rest-api/index/) |
| [List Topic Posts](actions/list-topic-posts.md) | `GET /forums/topics/:id/posts` | [docs](https://invisioncommunity.com/developers/rest-api/index/) |
| [List Topics](actions/list-topics.md) | `GET /forums/topics` | [docs](https://invisioncommunity.com/developers/rest-api/index/) |
| [List Transactions](actions/list-transactions.md) | `GET /nexus/transactions` | [docs](https://invisioncommunity.com/developers/rest-api/index/) |
| [List Venues](actions/list-venues.md) | `GET /calendar/venues` | [docs](https://invisioncommunity.com/developers/rest-api/index/) |
| [List Warn Reasons](actions/list-warn-reasons.md) | `GET /core/warnreasons` | [docs](https://invisioncommunity.com/developers/rest-api/index/) |
| [List Webhooks](actions/list-webhooks.md) | `GET /core/webhooks` | [docs](https://invisioncommunity.com/developers/rest-api/index/) |
| [List Withdrawals](actions/list-withdrawals.md) | `GET /nexus/withdrawals` | [docs](https://invisioncommunity.com/developers/rest-api/index/) |
| [Search Content](actions/search-content.md) | `GET /core/search` | [docs](https://invisioncommunity.com/developers/rest-api/index/) |

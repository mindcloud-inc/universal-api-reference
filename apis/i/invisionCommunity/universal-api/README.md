# <img src="https://images.mindcloud.co/apps/icons/invision-community_1775589375544.png" alt="Invision Community logo" width="28" height="28"> Invision Community: Universal API

Manage members, forums, blogs, commerce, files, galleries, events, and other community resources in Invision Community.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/invisionCommunity/latest
- **Category:** Marketing / Social Media
- **Actions:** 116
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://invisioncommunity.com/
- **Vendor API docs:** https://invisioncommunity.com/developers/rest-api/index/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Community Info](actions/get-community-info.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/invisionCommunity/latest/actions/get-community-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (116)

### Application

| Action | Method | Description |
| --- | --- | --- |
| [Get Applications](actions/get-applications.md) | GET |  |

### Assignment

| Action | Method | Description |
| --- | --- | --- |
| [List Assignments](actions/list-assignments.md) | GET |  |

### Blog

| Action | Method | Description |
| --- | --- | --- |
| [Get Blog](actions/get-blog.md) | GET |  |
| [List Blogs](actions/list-blogs.md) | GET |  |

### Blog Category

| Action | Method | Description |
| --- | --- | --- |
| [Get Blog Category](actions/get-blog-category.md) | GET |  |
| [List Blog Categories](actions/list-blog-categories.md) | GET |  |

### Blog Comment

| Action | Method | Description |
| --- | --- | --- |
| [Get Blog Comment](actions/get-blog-comment.md) | GET |  |
| [List Blog Comments](actions/list-blog-comments.md) | GET |  |
| [List Blog Entry Comments](actions/list-blog-entry-comments.md) | GET |  |

### Blog Entry

| Action | Method | Description |
| --- | --- | --- |
| [Get Blog Entry](actions/get-blog-entry.md) | GET |  |
| [List Blog Entries](actions/list-blog-entries.md) | GET |  |

### Blog Entry Category

| Action | Method | Description |
| --- | --- | --- |
| [Get Blog Entry Category](actions/get-blog-entry-category.md) | GET |  |
| [List Blog Entry Categories](actions/list-blog-entry-categories.md) | GET |  |

### Calendar

| Action | Method | Description |
| --- | --- | --- |
| [Get Calendar](actions/get-calendar.md) | GET |  |
| [List Calendars](actions/list-calendars.md) | GET |  |

### Calendar Comment

| Action | Method | Description |
| --- | --- | --- |
| [Get Calendar Comment](actions/get-calendar-comment.md) | GET |  |
| [List Calendar Comments](actions/list-calendar-comments.md) | GET |  |

### Calendar Review

| Action | Method | Description |
| --- | --- | --- |
| [Get Calendar Review](actions/get-calendar-review.md) | GET |  |
| [List Calendar Reviews](actions/list-calendar-reviews.md) | GET |  |

### Cloud Login Member

| Action | Method | Description |
| --- | --- | --- |
| [Get Cloud Login Handler Member](actions/get-cloud-login-handler-member.md) | GET |  |

### Club

| Action | Method | Description |
| --- | --- | --- |
| [Get Club](actions/get-club.md) | GET |  |
| [List Clubs](actions/list-clubs.md) | GET |  |

### Club Content Type

| Action | Method | Description |
| --- | --- | --- |
| [List Club Content Types](actions/list-club-content-types.md) | GET |  |

### Club Member

| Action | Method | Description |
| --- | --- | --- |
| [Get Club Member](actions/get-club-member.md) | GET |  |
| [List Club Members](actions/list-club-members.md) | GET |  |

### Club Node

| Action | Method | Description |
| --- | --- | --- |
| [List Club Nodes](actions/list-club-nodes.md) | GET |  |

### Cms Category

| Action | Method | Description |
| --- | --- | --- |
| [Get CMS Category](actions/get-cms-category.md) | GET |  |
| [List CMS Categories](actions/list-cms-categories.md) | GET |  |

### Cms Comment

| Action | Method | Description |
| --- | --- | --- |
| [Get CMS Comment](actions/get-cms-comment.md) | GET |  |
| [List CMS Comments](actions/list-cms-comments.md) | GET |  |

### Cms Database

| Action | Method | Description |
| --- | --- | --- |
| [Get CMS Database](actions/get-cms-database.md) | GET |  |
| [List CMS Databases](actions/list-cms-databases.md) | GET |  |

### Cms Record

| Action | Method | Description |
| --- | --- | --- |
| [Get CMS Record](actions/get-cms-record.md) | GET |  |
| [List CMS Records](actions/list-cms-records.md) | GET |  |

### Cms Record Comment

| Action | Method | Description |
| --- | --- | --- |
| [List CMS Record Comments](actions/list-cms-record-comments.md) | GET |  |

### Cms Record Review

| Action | Method | Description |
| --- | --- | --- |
| [List CMS Record Reviews](actions/list-cms-record-reviews.md) | GET |  |

### Cms Review

| Action | Method | Description |
| --- | --- | --- |
| [Get CMS Review](actions/get-cms-review.md) | GET |  |
| [List CMS Reviews](actions/list-cms-reviews.md) | GET |  |

### Community

| Action | Method | Description |
| --- | --- | --- |
| [Get Community Info](actions/get-community-info.md) | GET |  |

### Content Item

| Action | Method | Description |
| --- | --- | --- |
| [List Content Items](actions/list-content-items.md) | GET |  |

### Converter

| Action | Method | Description |
| --- | --- | --- |
| [List Converters](actions/list-converters.md) | GET |  |

### Course

| Action | Method | Description |
| --- | --- | --- |
| [Get Course](actions/get-course.md) | GET |  |
| [List Courses](actions/list-courses.md) | GET |  |

### Download Category

| Action | Method | Description |
| --- | --- | --- |
| [Get Download Category](actions/get-download-category.md) | GET |  |
| [List Download Categories](actions/list-download-categories.md) | GET |  |

### Download Comment

| Action | Method | Description |
| --- | --- | --- |
| [Get Download Comment](actions/get-download-comment.md) | GET |  |
| [List Download Comments](actions/list-download-comments.md) | GET |  |

### Download File

| Action | Method | Description |
| --- | --- | --- |
| [Get Download File](actions/get-download-file.md) | GET |  |
| [List Download Files](actions/list-download-files.md) | GET |  |

### Download File Comment

| Action | Method | Description |
| --- | --- | --- |
| [List Download File Comments](actions/list-download-file-comments.md) | GET |  |

### Download File History

| Action | Method | Description |
| --- | --- | --- |
| [List Download File History](actions/list-download-file-history.md) | GET |  |

### Download File Review

| Action | Method | Description |
| --- | --- | --- |
| [List Download File Reviews](actions/list-download-file-reviews.md) | GET |  |

### Download Review

| Action | Method | Description |
| --- | --- | --- |
| [Get Download Review](actions/get-download-review.md) | GET |  |
| [List Download Reviews](actions/list-download-reviews.md) | GET |  |

### Email Address

| Action | Method | Description |
| --- | --- | --- |
| [Get My Email](actions/get-my-email.md) | GET |  |

### Event

| Action | Method | Description |
| --- | --- | --- |
| [Get Event](actions/get-event.md) | GET |  |
| [List Events](actions/list-events.md) | GET |  |

### Event Comment

| Action | Method | Description |
| --- | --- | --- |
| [List Event Comments](actions/list-event-comments.md) | GET |  |

### Event Review

| Action | Method | Description |
| --- | --- | --- |
| [List Event Reviews](actions/list-event-reviews.md) | GET |  |

### Event Rsvp

| Action | Method | Description |
| --- | --- | --- |
| [Get Event RSVP](actions/get-event-rsvp.md) | GET |  |
| [List Event RSVPs](actions/list-event-rsvps.md) | GET |  |

### Featured Content

| Action | Method | Description |
| --- | --- | --- |
| [Get Featured Content](actions/get-featured-content.md) | GET |  |
| [List Featured Content](actions/list-featured-content.md) | GET |  |

### Forum

| Action | Method | Description |
| --- | --- | --- |
| [Get Forum](actions/get-forum.md) | GET |  |
| [List Forums](actions/list-forums.md) | GET |  |

### Gallery Album

| Action | Method | Description |
| --- | --- | --- |
| [Get Gallery Album](actions/get-gallery-album.md) | GET |  |
| [List Gallery Albums](actions/list-gallery-albums.md) | GET |  |

### Gallery Category

| Action | Method | Description |
| --- | --- | --- |
| [Get Gallery Category](actions/get-gallery-category.md) | GET |  |
| [List Gallery Categories](actions/list-gallery-categories.md) | GET |  |

### Gallery Comment

| Action | Method | Description |
| --- | --- | --- |
| [Get Gallery Comment](actions/get-gallery-comment.md) | GET |  |
| [List Gallery Comments](actions/list-gallery-comments.md) | GET |  |

### Gallery Review

| Action | Method | Description |
| --- | --- | --- |
| [Get Gallery Review](actions/get-gallery-review.md) | GET |  |
| [List Gallery Reviews](actions/list-gallery-reviews.md) | GET |  |

### Group

| Action | Method | Description |
| --- | --- | --- |
| [Get Group](actions/get-group.md) | GET |  |
| [List Groups](actions/list-groups.md) | GET |  |

### Image

| Action | Method | Description |
| --- | --- | --- |
| [Get Image](actions/get-image.md) | GET |  |
| [List Images](actions/list-images.md) | GET |  |

### Image Comment

| Action | Method | Description |
| --- | --- | --- |
| [List Image Comments](actions/list-image-comments.md) | GET |  |

### Image Review

| Action | Method | Description |
| --- | --- | --- |
| [List Image Reviews](actions/list-image-reviews.md) | GET |  |

### Invoice

| Action | Method | Description |
| --- | --- | --- |
| [Get Invoice](actions/get-invoice.md) | GET |  |
| [List Invoices](actions/list-invoices.md) | GET |  |

### License Key

| Action | Method | Description |
| --- | --- | --- |
| [Get License Key](actions/get-license-key.md) | GET |  |

### Member

| Action | Method | Description |
| --- | --- | --- |
| [Get Member](actions/get-member.md) | GET |  |
| [List Members](actions/list-members.md) | GET |  |

### Member Follow

| Action | Method | Description |
| --- | --- | --- |
| [Get Member Follow](actions/get-member-follow.md) | GET |  |
| [List Member Follows](actions/list-member-follows.md) | GET |  |

### Member Message

| Action | Method | Description |
| --- | --- | --- |
| [List Member Messages](actions/list-member-messages.md) | GET |  |

### Member Notification

| Action | Method | Description |
| --- | --- | --- |
| [List Member Notifications](actions/list-member-notifications.md) | GET |  |

### Member Warning

| Action | Method | Description |
| --- | --- | --- |
| [Get Member Warning](actions/get-member-warning.md) | GET |  |
| [List Member Warnings](actions/list-member-warnings.md) | GET |  |

### Message

| Action | Method | Description |
| --- | --- | --- |
| [Get Message](actions/get-message.md) | GET |  |
| [List Messages](actions/list-messages.md) | GET |  |

### Message Reply

| Action | Method | Description |
| --- | --- | --- |
| [Get Message Reply](actions/get-message-reply.md) | GET |  |
| [List Message Replies](actions/list-message-replies.md) | GET |  |

### Post

| Action | Method | Description |
| --- | --- | --- |
| [Get Post](actions/get-post.md) | GET |  |
| [List Posts](actions/list-posts.md) | GET |  |

### Profile

| Action | Method | Description |
| --- | --- | --- |
| [Get My Profile](actions/get-my-profile.md) | GET |  |

### Purchase

| Action | Method | Description |
| --- | --- | --- |
| [Get Purchase](actions/get-purchase.md) | GET |  |
| [List Purchases](actions/list-purchases.md) | GET |  |

### Search Content Type

| Action | Method | Description |
| --- | --- | --- |
| [List Search Content Types](actions/list-search-content-types.md) | GET |  |

### Search Result

| Action | Method | Description |
| --- | --- | --- |
| [Search Content](actions/search-content.md) | GET |  |

### Tag

| Action | Method | Description |
| --- | --- | --- |
| [Get Tag](actions/get-tag.md) | GET |  |
| [List Tags](actions/list-tags.md) | GET |  |

### Topic

| Action | Method | Description |
| --- | --- | --- |
| [Get Topic](actions/get-topic.md) | GET |  |
| [List Topics](actions/list-topics.md) | GET |  |

### Topic Post

| Action | Method | Description |
| --- | --- | --- |
| [List Topic Posts](actions/list-topic-posts.md) | GET |  |

### Transaction

| Action | Method | Description |
| --- | --- | --- |
| [Get Transaction](actions/get-transaction.md) | GET |  |
| [List Transactions](actions/list-transactions.md) | GET |  |

### Venue

| Action | Method | Description |
| --- | --- | --- |
| [Get Venue](actions/get-venue.md) | GET |  |
| [List Venues](actions/list-venues.md) | GET |  |

### Warn Reason

| Action | Method | Description |
| --- | --- | --- |
| [Get Warn Reason](actions/get-warn-reason.md) | GET |  |
| [List Warn Reasons](actions/list-warn-reasons.md) | GET |  |

### Webhook

| Action | Method | Description |
| --- | --- | --- |
| [Get Webhook](actions/get-webhook.md) | GET |  |
| [List Webhooks](actions/list-webhooks.md) | GET |  |

### Withdrawal

| Action | Method | Description |
| --- | --- | --- |
| [Get Withdrawal](actions/get-withdrawal.md) | GET |  |
| [List Withdrawals](actions/list-withdrawals.md) | GET |  |


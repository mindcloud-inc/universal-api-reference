# Invision Community Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Invision Community expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/invisionCommunity/latest/actions/list-assignments?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Invision Community actions that support pagination

- [List Assignments](actions/list-assignments.md)
- [List Blog Categories](actions/list-blog-categories.md)
- [List Blog Comments](actions/list-blog-comments.md)
- [List Blog Entries](actions/list-blog-entries.md)
- [List Blog Entry Categories](actions/list-blog-entry-categories.md)
- [List Blog Entry Comments](actions/list-blog-entry-comments.md)
- [List Blogs](actions/list-blogs.md)
- [List Calendar Comments](actions/list-calendar-comments.md)
- [List Calendar Reviews](actions/list-calendar-reviews.md)
- [List Calendars](actions/list-calendars.md)
- [List Club Members](actions/list-club-members.md)
- [List Club Nodes](actions/list-club-nodes.md)
- [List Clubs](actions/list-clubs.md)
- [List CMS Categories](actions/list-cms-categories.md)
- [List CMS Comments](actions/list-cms-comments.md)
- [List CMS Record Comments](actions/list-cms-record-comments.md)
- [List CMS Record Reviews](actions/list-cms-record-reviews.md)
- [List CMS Records](actions/list-cms-records.md)
- [List CMS Reviews](actions/list-cms-reviews.md)
- [List Content Items](actions/list-content-items.md)
- [List Courses](actions/list-courses.md)
- [List Download Categories](actions/list-download-categories.md)
- [List Download Comments](actions/list-download-comments.md)
- [List Download File Comments](actions/list-download-file-comments.md)
- [List Download File History](actions/list-download-file-history.md)
- [List Download File Reviews](actions/list-download-file-reviews.md)
- [List Download Files](actions/list-download-files.md)
- [List Download Reviews](actions/list-download-reviews.md)
- [List Event Comments](actions/list-event-comments.md)
- [List Event Reviews](actions/list-event-reviews.md)
- [List Event RSVPs](actions/list-event-rsvps.md)
- [List Events](actions/list-events.md)
- [List Featured Content](actions/list-featured-content.md)
- [List Forums](actions/list-forums.md)
- [List Gallery Albums](actions/list-gallery-albums.md)
- [List Gallery Categories](actions/list-gallery-categories.md)
- [List Gallery Comments](actions/list-gallery-comments.md)
- [List Gallery Reviews](actions/list-gallery-reviews.md)
- [List Image Comments](actions/list-image-comments.md)
- [List Image Reviews](actions/list-image-reviews.md)
- [List Images](actions/list-images.md)
- [List Invoices](actions/list-invoices.md)
- [List Member Follows](actions/list-member-follows.md)
- [List Member Messages](actions/list-member-messages.md)
- [List Member Notifications](actions/list-member-notifications.md)
- [List Member Warnings](actions/list-member-warnings.md)
- [List Members](actions/list-members.md)
- [List Message Replies](actions/list-message-replies.md)
- [List Messages](actions/list-messages.md)
- [List Posts](actions/list-posts.md)
- [List Purchases](actions/list-purchases.md)
- [List Tags](actions/list-tags.md)
- [List Topic Posts](actions/list-topic-posts.md)
- [List Topics](actions/list-topics.md)
- [List Transactions](actions/list-transactions.md)
- [List Venues](actions/list-venues.md)
- [List Webhooks](actions/list-webhooks.md)
- [List Withdrawals](actions/list-withdrawals.md)
- [Search Content](actions/search-content.md)

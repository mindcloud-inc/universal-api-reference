# <img src="https://images.mindcloud.co/apps/icons/productlift-icon_1776693849919.png" alt="ProductLift logo" width="28" height="28"> ProductLift: Universal API

ProductLift is a customer feedback, roadmap, changelog, and product vision platform for collecting ideas, managing posts and comments, organizing categories, tabs, sections, statuses, groups, tags, users, and moderation workflows through a REST API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/productLift/latest
- **Category:** Support / Customer Success
- **Actions:** 75
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.productlift.dev
- **Vendor API docs:** https://developer.productlift.dev/api/documentation/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Portal](actions/get-portal.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/productLift/latest/actions/get-portal?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (75)

### Anonymous Vote

| Action | Method | Description |
| --- | --- | --- |
| [Revoke Anonymous Vote](actions/revoke-anonymous-vote.md) | DELETE |  |
| [Vote Anonymously](actions/vote-anonymously.md) | POST |  |

### Category

| Action | Method | Description |
| --- | --- | --- |
| [Create Category](actions/create-category.md) | POST |  |
| [Delete Category](actions/delete-category.md) | DELETE |  |
| [List Categories](actions/list-categories.md) | GET |  |
| [Update Category](actions/update-category.md) | PUT |  |

### Comment

| Action | Method | Description |
| --- | --- | --- |
| [Create Comment](actions/create-comment.md) | POST |  |
| [Delete Comment](actions/delete-comment.md) | DELETE |  |
| [List Comments](actions/list-comments.md) | GET |  |
| [Update Comment](actions/update-comment.md) | PUT |  |

### Feedback

| Action | Method | Description |
| --- | --- | --- |
| [Create Feedback](actions/create-feedback.md) | POST |  |
| [Delete Feedback](actions/delete-feedback.md) | DELETE |  |
| [List Feedback](actions/list-feedback.md) | GET |  |
| [Update Feedback](actions/update-feedback.md) | PUT |  |

### Feedback Summary

| Action | Method | Description |
| --- | --- | --- |
| [Summarize Feedback](actions/summarize-feedback.md) | GET |  |

### Group

| Action | Method | Description |
| --- | --- | --- |
| [Create Group](actions/create-group.md) | POST |  |
| [Delete Group](actions/delete-group.md) | DELETE |  |
| [Get Group](actions/get-group.md) | GET |  |
| [List Groups](actions/list-groups.md) | GET |  |
| [Update Group](actions/update-group.md) | PUT |  |

### Group Membership

| Action | Method | Description |
| --- | --- | --- |
| [Add User To Group](actions/add-user-to-group.md) | POST |  |
| [Remove User From Group](actions/remove-user-from-group.md) | DELETE |  |

### Group User

| Action | Method | Description |
| --- | --- | --- |
| [List Group Users](actions/list-group-users.md) | GET |  |

### Moderation Item

| Action | Method | Description |
| --- | --- | --- |
| [Approve Moderation Item](actions/approve-moderation-item.md) | PUT |  |
| [List Pending Moderation Items](actions/list-pending-moderation-items.md) | GET |  |
| [List Rejected Moderation Items](actions/list-rejected-moderation-items.md) | GET |  |
| [Reject Moderation Item](actions/reject-moderation-item.md) | PUT |  |

### Plan Type

| Action | Method | Description |
| --- | --- | --- |
| [List User Plan Types](actions/list-user-plan-types.md) | GET |  |

### Portal

| Action | Method | Description |
| --- | --- | --- |
| [Get Portal](actions/get-portal.md) | GET |  |

### Post

| Action | Method | Description |
| --- | --- | --- |
| [Adjust Post Text](actions/adjust-post-text.md) | PUT |  |
| [Create Post](actions/create-post.md) | POST |  |
| [Delete Post](actions/delete-post.md) | DELETE |  |
| [Get Post](actions/get-post.md) | GET |  |
| [Improve Post Writing](actions/improve-post-writing.md) | PUT |  |
| [List Posts](actions/list-posts.md) | GET |  |
| [List Posts For Tab](actions/list-posts-for-tab.md) | GET |  |
| [Search Duplicate Posts](actions/search-duplicate-posts.md) | GET |  |
| [Search Posts Within Tab](actions/search-posts-within-tab.md) | GET |  |
| [Toggle Post Publish](actions/toggle-post-publish.md) | PUT |  |
| [Update Post](actions/update-post.md) | PUT |  |

### Product Vision

| Action | Method | Description |
| --- | --- | --- |
| [Create Or Update Product Vision](actions/create-or-update-product-vision.md) | PUT |  |
| [Delete Product Vision](actions/delete-product-vision.md) | DELETE |  |
| [Generate Product Vision](actions/generate-product-vision.md) | POST |  |
| [Get Product Vision](actions/get-product-vision.md) | GET |  |

### Section

| Action | Method | Description |
| --- | --- | --- |
| [Create Section](actions/create-section.md) | POST |  |
| [Delete Section](actions/delete-section.md) | DELETE |  |
| [List Child Sections](actions/list-child-sections.md) | GET |  |
| [List Root Sections](actions/list-root-sections.md) | GET |  |
| [Update Section](actions/update-section.md) | PUT |  |

### Segment Metadata Key

| Action | Method | Description |
| --- | --- | --- |
| [List User Segment Metadata Keys](actions/list-user-segment-metadata-keys.md) | GET |  |

### Status

| Action | Method | Description |
| --- | --- | --- |
| [Create Status](actions/create-status.md) | POST |  |
| [Delete Status](actions/delete-status.md) | DELETE |  |
| [List Statuses](actions/list-statuses.md) | GET |  |
| [Update Status](actions/update-status.md) | PUT |  |

### Tab

| Action | Method | Description |
| --- | --- | --- |
| [Get Tab](actions/get-tab.md) | GET |  |
| [List Tabs](actions/list-tabs.md) | GET |  |

### Tag

| Action | Method | Description |
| --- | --- | --- |
| [Create Tag](actions/create-tag.md) | POST |  |
| [Delete Tag](actions/delete-tag.md) | DELETE |  |
| [List Tags](actions/list-tags.md) | GET |  |
| [Update Tag](actions/update-tag.md) | PUT |  |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Bulk Block Users](actions/bulk-block-users.md) | PUT |  |
| [Bulk Delete Users](actions/bulk-delete-users.md) | DELETE |  |
| [Bulk Unblock Users](actions/bulk-unblock-users.md) | PUT |  |
| [Create User](actions/create-user.md) | POST |  |
| [Delete User](actions/delete-user.md) | DELETE |  |
| [Find User By Email](actions/find-user-by-email.md) | GET |  |
| [Get User](actions/get-user.md) | GET |  |
| [List Users](actions/list-users.md) | GET |  |
| [Update User](actions/update-user.md) | PUT |  |

### User Group Filter

| Action | Method | Description |
| --- | --- | --- |
| [List User Group Filters](actions/list-user-group-filters.md) | GET |  |

### Vote

| Action | Method | Description |
| --- | --- | --- |
| [List Post Votes](actions/list-post-votes.md) | GET |  |
| [Revoke User Vote](actions/revoke-user-vote.md) | DELETE |  |
| [Vote With User](actions/vote-with-user.md) | POST |  |

### Widget

| Action | Method | Description |
| --- | --- | --- |
| [Get Widget](actions/get-widget.md) | GET |  |
| [List Widgets](actions/list-widgets.md) | GET |  |


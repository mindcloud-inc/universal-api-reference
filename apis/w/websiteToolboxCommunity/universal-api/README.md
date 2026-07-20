# <img src="https://images.mindcloud.co/apps/icons/website-toolbox-community-icon_1775660563987.png" alt="Website Toolbox Community logo" width="28" height="28"> Website Toolbox Community: Universal API

Website Toolbox Community wraps the Website Toolbox REST API for managing community categories, moderators, conversations, messages, posts, topics, user groups, users, and related forum resources.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/websiteToolboxCommunity/latest
- **Actions:** 35
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.websitetoolbox.com
- **Vendor API docs:** https://www.websitetoolbox.com/docs/api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Categories](actions/list-categories.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/websiteToolboxCommunity/latest/actions/list-categories?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (35)

### Category

| Action | Method | Description |
| --- | --- | --- |
| [Create Category](actions/create-category.md) | POST |  |
| [Delete Category](actions/delete-category.md) | DELETE |  |
| [Get Category](actions/get-category.md) | GET |  |
| [List Categories](actions/list-categories.md) | GET |  |
| [Update Category](actions/update-category.md) | PUT |  |

### Category Permission

| Action | Method | Description |
| --- | --- | --- |
| [List Category Permissions](actions/list-category-permissions.md) | GET |  |
| [Update Category Permission](actions/update-category-permission.md) | PUT |  |

### Conversation

| Action | Method | Description |
| --- | --- | --- |
| [Create Conversation](actions/create-conversation.md) | POST |  |
| [Delete Conversation](actions/delete-conversation.md) | DELETE |  |
| [Get Conversation](actions/get-conversation.md) | GET |  |
| [List Conversations](actions/list-conversations.md) | GET |  |

### Message

| Action | Method | Description |
| --- | --- | --- |
| [Create Message](actions/create-message.md) | POST |  |
| [Get Message](actions/get-message.md) | GET |  |
| [List Messages](actions/list-messages.md) | GET |  |

### Moderator

| Action | Method | Description |
| --- | --- | --- |
| [Create Moderator](actions/create-moderator.md) | POST |  |
| [Delete Moderator](actions/delete-moderator.md) | DELETE |  |
| [Get Moderator](actions/get-moderator.md) | GET |  |
| [List Moderators](actions/list-moderators.md) | GET |  |
| [Update Moderator](actions/update-moderator.md) | PUT |  |

### Page View

| Action | Method | Description |
| --- | --- | --- |
| [List Page Views](actions/list-page-views.md) | GET |  |

### Post

| Action | Method | Description |
| --- | --- | --- |
| [Create Post](actions/create-post.md) | POST |  |
| [Delete Post](actions/delete-post.md) | DELETE |  |
| [Get Post](actions/get-post.md) | GET |  |
| [List Posts](actions/list-posts.md) | GET |  |
| [Update Post](actions/update-post.md) | PUT |  |

### Tag

| Action | Method | Description |
| --- | --- | --- |
| [List Tags](actions/list-tags.md) | GET |  |

### Topic

| Action | Method | Description |
| --- | --- | --- |
| [Create Topic](actions/create-topic.md) | POST |  |
| [Delete Topic](actions/delete-topic.md) | DELETE |  |
| [Get Topic](actions/get-topic.md) | GET |  |
| [List Topics](actions/list-topics.md) | GET |  |
| [Update Topic](actions/update-topic.md) | PUT |  |

### User Group

| Action | Method | Description |
| --- | --- | --- |
| [Create User Group](actions/create-user-group.md) | POST |  |
| [Get User Group](actions/get-user-group.md) | GET |  |
| [List User Groups](actions/list-user-groups.md) | GET |  |
| [Update User Group](actions/update-user-group.md) | PUT |  |


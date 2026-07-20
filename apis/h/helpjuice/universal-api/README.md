# <img src="https://images.mindcloud.co/apps/icons/images-5_1774036135639.png" alt="Helpjuice logo" width="28" height="28"> Helpjuice: Universal API

Manage Helpjuice knowledge base articles, categories, users, settings, and webhooks.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/helpjuice/latest
- **Category:** Productivity / Knowledge Management
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://helpjuice.com/
- **Vendor API docs:** https://help.helpjuice.com/using-api-v3

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Account Settings](actions/get-account-settings.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/helpjuice/latest/actions/get-account-settings?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### Account

| Action | Method | Description |
| --- | --- | --- |
| [Get Account Settings](actions/get-account-settings.md) | GET | Retrieves account settings from Helpjuice. |

### Activity

| Action | Method | Description |
| --- | --- | --- |
| [Get Activity](actions/get-activity.md) | GET | Retrieves an activity from Helpjuice. |
| [List Activities](actions/list-activities.md) | GET | Retrieves activities from Helpjuice. |

### Article

| Action | Method | Description |
| --- | --- | --- |
| [Create Article](actions/create-article.md) | POST | Creates a new article in Helpjuice. |
| [Delete Article](actions/delete-article.md) | DELETE | Deletes an existing article from Helpjuice. |
| [Downvote Article](actions/downvote-article.md) | PUT | Downvotes an article in Helpjuice. |
| [Get Article](actions/get-article.md) | GET | Retrieves an article from Helpjuice. |
| [List Articles](actions/list-articles.md) | GET | Retrieves articles from Helpjuice. |
| [Update Article](actions/update-article.md) | PUT | Updates an existing article in Helpjuice. |
| [Upvote Article](actions/upvote-article.md) | PUT | Upvotes an article in Helpjuice. |

### Article Analytics

| Action | Method | Description |
| --- | --- | --- |
| [List Article Analytics](actions/list-article-analytics.md) | GET | Retrieves article analytics from Helpjuice. |

### Backup

| Action | Method | Description |
| --- | --- | --- |
| [List Backups](actions/list-backups.md) | GET | Retrieves backups from Helpjuice. |

### Category

| Action | Method | Description |
| --- | --- | --- |
| [Create Category](actions/create-category.md) | POST | Creates a new category in Helpjuice. |
| [Get Category](actions/get-category.md) | GET | Retrieves a category from Helpjuice. |
| [List Categories](actions/list-categories.md) | GET | Retrieves categories from Helpjuice. |
| [List Category Analytics](actions/list-category-analytics.md) | GET | Retrieves category analytics from Helpjuice. |
| [Update Category](actions/update-category.md) | PUT | Updates an existing category in Helpjuice. |

### Group

| Action | Method | Description |
| --- | --- | --- |
| [Create Group](actions/create-group.md) | POST | Creates a new group in Helpjuice. |
| [Delete Group](actions/delete-group.md) | DELETE | Deletes an existing group from Helpjuice. |
| [Get Group](actions/get-group.md) | GET | Retrieves a group from Helpjuice. |
| [List Group Analytics](actions/list-group-analytics.md) | GET | Retrieves group analytics from Helpjuice. |
| [List Groups](actions/list-groups.md) | GET | Retrieves groups from Helpjuice. |
| [Update Group](actions/update-group.md) | PUT | Updates an existing group in Helpjuice. |

### Search Analytics

| Action | Method | Description |
| --- | --- | --- |
| [List Search Analytics](actions/list-search-analytics.md) | GET | Retrieves search analytics from Helpjuice. |

### Search Result

| Action | Method | Description |
| --- | --- | --- |
| [Search KB](actions/search-kb.md) | GET | Finds articles in Helpjuice by search query. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Activate User](actions/activate-user.md) | PUT | Activates a user in Helpjuice. |
| [Create User](actions/create-user.md) | POST | Creates a new user in Helpjuice. |
| [Deactivate User](actions/deactivate-user.md) | PUT | Deactivates a user in Helpjuice. |
| [Delete User](actions/delete-user.md) | DELETE | Deletes an existing user from Helpjuice. |
| [Get User](actions/get-user.md) | GET | Retrieves a user from Helpjuice. |
| [List Group Users](actions/list-group-users.md) | GET | Retrieves users in a Helpjuice group. |
| [List User Analytics](actions/list-user-analytics.md) | GET | Retrieves user analytics from Helpjuice. |
| [List Users](actions/list-users.md) | GET | Retrieves users from Helpjuice. |
| [Update User](actions/update-user.md) | PUT | Updates an existing user in Helpjuice. |

### Webhook Event

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook](actions/create-webhook.md) | POST | Creates a new webhook in Helpjuice. |
| [Delete Webhook](actions/delete-webhook.md) | DELETE | Deletes an existing webhook from Helpjuice. |
| [Get Webhook](actions/get-webhook.md) | GET | Retrieves a webhook from Helpjuice. |
| [List Webhooks](actions/list-webhooks.md) | GET | Retrieves webhooks from Helpjuice. |
| [Test Webhook](actions/test-webhook.md) | POST | Tests a webhook in Helpjuice. |
| [Toggle Webhook](actions/toggle-webhook.md) | PUT | Toggles a webhook in Helpjuice. |


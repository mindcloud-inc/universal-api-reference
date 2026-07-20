# <img src="https://images.mindcloud.co/apps/icons/inoreader_1773681080059.png" alt="Inoreader logo" width="28" height="28"> Inoreader: Universal API

Read and manage Inoreader subscriptions, streams, tags, unread counts, and article state through the official Inoreader developer API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/inoreader/latest
- **Actions:** 13
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.inoreader.com/
- **Vendor API docs:** https://www.inoreader.com/developers/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get User Information](actions/get-user-information.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/inoreader/latest/actions/get-user-information?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (13)

### Article

| Action | Method | Description |
| --- | --- | --- |
| [List Stream Contents](actions/list-stream-contents.md) | GET | Retrieves contents from a specific Inoreader stream. |
| [List Stream Item IDs](actions/list-stream-item-ids.md) | GET | Retrieves item IDs from an Inoreader stream. |
| [Mark Stream As Read](actions/mark-stream-as-read.md) | PUT | Marks an Inoreader stream as read. |
| [Update Article Tags](actions/update-article-tags.md) | PUT | Updates article tags in Inoreader. |

### Stream Preference

| Action | Method | Description |
| --- | --- | --- |
| [List Stream Preferences](actions/list-stream-preferences.md) | GET | Retrieves stream preferences from Inoreader. |

### Subscription

| Action | Method | Description |
| --- | --- | --- |
| [Add Feed](actions/add-feed.md) | POST | Adds a new feed subscription in Inoreader. |
| [List Feeds](actions/list-feeds.md) | GET | Retrieves feed subscriptions from Inoreader. |
| [Update Feed](actions/update-feed.md) | PUT | Updates an existing feed subscription in Inoreader. |

### Tag

| Action | Method | Description |
| --- | --- | --- |
| [Delete Tag](actions/delete-tag.md) | DELETE | Deletes an existing tag from Inoreader. |
| [List Folders and Tags](actions/list-folders-and-tags.md) | GET | Retrieves folders and tags from Inoreader. |
| [Rename Tag](actions/rename-tag.md) | PUT | Renames an existing tag in Inoreader. |

### Unread Count

| Action | Method | Description |
| --- | --- | --- |
| [List Unread Counters](actions/list-unread-counters.md) | GET | Retrieves unread counters from Inoreader. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get User Information](actions/get-user-information.md) | GET | Retrieves the current user information from Inoreader. |


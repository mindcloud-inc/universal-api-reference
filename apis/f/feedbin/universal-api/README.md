# <img src="https://images.mindcloud.co/apps/icons/feedbin_1776277720212.png" alt="Feedbin logo" width="28" height="28"> Feedbin: Universal API

Feedbin is an RSS reader for subscribing to feeds, reading entries, and managing unread, starred, and tagged articles.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/feedbin/latest
- **Category:** Productivity / Knowledge Management
- **Actions:** 25
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://feedbin.com
- **Vendor API docs:** https://github.com/feedbin/feedbin-api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Subscriptions](actions/list-subscriptions.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/feedbin/latest/actions/list-subscriptions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (25)

### Assets

| Action | Method | Description |
| --- | --- | --- |
| [List Feed Icons](actions/list-feed-icons.md) | GET | Retrieves feed icons for subscriptions from Feedbin. |

### Items

| Action | Method | Description |
| --- | --- | --- |
| [Get Entry](actions/get-entry.md) | GET | Retrieves a single entry from Feedbin. |
| [List Entries](actions/list-entries.md) | GET | Retrieves a list of entries from Feedbin. |
| [List Feed Entries](actions/list-feed-entries.md) | GET | Retrieves entries for a specific feed from Feedbin. |
| [List Starred Entry IDs](actions/list-starred-entry-ids.md) | GET | Retrieves starred entry IDs from Feedbin. |
| [List Unread Entry IDs](actions/list-unread-entry-ids.md) | GET | Retrieves unread entry IDs from Feedbin. |
| [Mark Entries Read](actions/mark-entries-read.md) | PUT | Marks entries as read in Feedbin. |
| [Mark Entries Unread](actions/mark-entries-unread.md) | PUT | Marks entries as unread in Feedbin. |
| [Star Entries](actions/star-entries.md) | PUT | Marks entries as starred in Feedbin. |
| [Unstar Entries](actions/unstar-entries.md) | PUT | Removes starred status from entries in Feedbin. |

### Queries

| Action | Method | Description |
| --- | --- | --- |
| [Create Saved Search](actions/create-saved-search.md) | POST | Creates a new saved search in Feedbin. |
| [Delete Saved Search](actions/delete-saved-search.md) | DELETE | Deletes an existing saved search from Feedbin. |
| [List Saved Searches](actions/list-saved-searches.md) | GET | Retrieves a list of saved searches from Feedbin. |
| [Run Saved Search](actions/run-saved-search.md) | GET | Retrieves saved search results from Feedbin. |
| [Update Saved Search](actions/update-saved-search.md) | PUT | Updates an existing saved search in Feedbin. |

### Subscriptions

| Action | Method | Description |
| --- | --- | --- |
| [Create Subscription](actions/create-subscription.md) | POST | Creates a new subscription in Feedbin. |
| [Delete Subscription](actions/delete-subscription.md) | DELETE | Deletes an existing subscription from Feedbin. |
| [Get Subscription](actions/get-subscription.md) | GET | Retrieves a single subscription from Feedbin. |
| [List Subscriptions](actions/list-subscriptions.md) | GET | Retrieves a list of subscriptions from Feedbin. |
| [Update Subscription](actions/update-subscription.md) | PUT | Updates an existing subscription in Feedbin. |

### Tags

| Action | Method | Description |
| --- | --- | --- |
| [Create Tagging](actions/create-tagging.md) | POST | Creates a new tagging in Feedbin. |
| [Delete Tagging](actions/delete-tagging.md) | DELETE | Deletes an existing tagging from Feedbin. |
| [Get Tagging](actions/get-tagging.md) | GET | Retrieves a single tagging from Feedbin. |
| [List Taggings](actions/list-taggings.md) | GET | Retrieves a list of taggings from Feedbin. |
| [Rename Tag](actions/rename-tag.md) | PUT | Renames an existing tag in Feedbin. |


# Feedbin: Native API Reference

A consolidated summary of Feedbin's API configuration and 25 documented operations, with links to official documentation.

- **Official docs:** https://github.com/feedbin/feedbin-api
- **API base URL:** `https://api.feedbin.com/v2`

## Authentication

### Basic Auth

Authenticate with the Feedbin account email and password using HTTP Basic authentication.

### Credentials

- **Username:** `username` · required
- **Password:** `password` · required

Join the username and password with a colon, Base64-encode the result, and send it with the `Basic` authorization scheme:

```js
const credentials = Buffer.from(`${username}:${password}`).toString('base64');

const response = await fetch(url, {
  headers: {
    Authorization: `Basic ${credentials}`
  }
});
```

[Official authentication documentation](https://github.com/feedbin/feedbin-api#making-requests)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json; charset=utf-8` |

Responses from this API use JSON.

## Pagination

Use `per_page` in the query string to set the page size (default 50; accepted range 1–100). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (25 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Saved Search](actions/create-saved-search.md) | `POST saved_searches.json` | [docs](https://github.com/feedbin/feedbin-api/blob/master/content/saved-searches.md#create-saved-search) |
| [Create Subscription](actions/create-subscription.md) | `POST subscriptions.json` | [docs](https://github.com/feedbin/feedbin-api/blob/master/content/subscriptions.md#create-subscription) |
| [Create Tagging](actions/create-tagging.md) | `POST taggings.json` | [docs](https://github.com/feedbin/feedbin-api/blob/master/content/taggings.md#create-tagging) |
| [Delete Saved Search](actions/delete-saved-search.md) | `DELETE saved_searches/[:id].json` | [docs](https://github.com/feedbin/feedbin-api/blob/master/content/saved-searches.md#delete-saved-search) |
| [Delete Subscription](actions/delete-subscription.md) | `DELETE subscriptions/[:id].json` | [docs](https://github.com/feedbin/feedbin-api/blob/master/content/subscriptions.md#delete-subscription) |
| [Delete Tagging](actions/delete-tagging.md) | `DELETE taggings/[:id].json` | [docs](https://github.com/feedbin/feedbin-api/blob/master/content/taggings.md#delete-tagging) |
| [Get Entry](actions/get-entry.md) | `GET entries/[:id].json` | [docs](https://github.com/feedbin/feedbin-api/blob/master/content/entries.md#get-v2entries3648json) |
| [Get Subscription](actions/get-subscription.md) | `GET subscriptions/[:id].json` | [docs](https://github.com/feedbin/feedbin-api/blob/master/content/subscriptions.md#get-subscription) |
| [Get Tagging](actions/get-tagging.md) | `GET taggings/[:id].json` | [docs](https://github.com/feedbin/feedbin-api/blob/master/content/taggings.md#get-tagging) |
| [List Entries](actions/list-entries.md) | `GET entries.json` | [docs](https://github.com/feedbin/feedbin-api/blob/master/content/entries.md#get-v2entriesjson) |
| [List Feed Entries](actions/list-feed-entries.md) | `GET feeds/[:feed_id]/entries.json` | [docs](https://github.com/feedbin/feedbin-api/blob/master/content/entries.md#get-v2feeds203entriesjson) |
| [List Feed Icons](actions/list-feed-icons.md) | `GET icons.json` | [docs](https://github.com/feedbin/feedbin-api/blob/master/content/icons.md#get-v2iconsjson) |
| [List Saved Searches](actions/list-saved-searches.md) | `GET saved_searches.json` | [docs](https://github.com/feedbin/feedbin-api/blob/master/content/saved-searches.md#get-saved-searches) |
| [List Starred Entry IDs](actions/list-starred-entry-ids.md) | `GET starred_entries.json` | [docs](https://github.com/feedbin/feedbin-api/blob/master/content/starred-entries.md#get-starred-entries) |
| [List Subscriptions](actions/list-subscriptions.md) | `GET subscriptions.json` | [docs](https://github.com/feedbin/feedbin-api/blob/master/content/subscriptions.md#get-subscriptions) |
| [List Taggings](actions/list-taggings.md) | `GET taggings.json` | [docs](https://github.com/feedbin/feedbin-api/blob/master/content/taggings.md#get-taggings) |
| [List Unread Entry IDs](actions/list-unread-entry-ids.md) | `GET unread_entries.json` | [docs](https://github.com/feedbin/feedbin-api/blob/master/content/unread-entries.md#get-unread-entries) |
| [Mark Entries Read](actions/mark-entries-read.md) | `DELETE unread_entries.json` | [docs](https://github.com/feedbin/feedbin-api/blob/master/content/unread-entries.md#delete-unread-entries-mark-as-read) |
| [Mark Entries Unread](actions/mark-entries-unread.md) | `POST unread_entries.json` | [docs](https://github.com/feedbin/feedbin-api/blob/master/content/unread-entries.md#create-unread-entries-mark-as-unread) |
| [Rename Tag](actions/rename-tag.md) | `POST tags.json` | [docs](https://github.com/feedbin/feedbin-api/blob/master/content/tags.md#post-v2tagsjson) |
| [Run Saved Search](actions/run-saved-search.md) | `GET saved_searches/[:id].json` | [docs](https://github.com/feedbin/feedbin-api/blob/master/content/saved-searches.md#get-saved-search) |
| [Star Entries](actions/star-entries.md) | `POST starred_entries.json` | [docs](https://github.com/feedbin/feedbin-api/blob/master/content/starred-entries.md#create-starred-entries) |
| [Unstar Entries](actions/unstar-entries.md) | `DELETE starred_entries.json` | [docs](https://github.com/feedbin/feedbin-api/blob/master/content/starred-entries.md#delete-starred-entries-unstar) |
| [Update Saved Search](actions/update-saved-search.md) | `PATCH saved_searches/[:id].json` | [docs](https://github.com/feedbin/feedbin-api/blob/master/content/saved-searches.md#update-saved-search) |
| [Update Subscription](actions/update-subscription.md) | `PATCH subscriptions/[:id].json` | [docs](https://github.com/feedbin/feedbin-api/blob/master/content/subscriptions.md#update-subscription) |

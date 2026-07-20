# Mark Entries Unread with Feedbin

Marks entries as unread in Feedbin.

## Endpoint

- **Method:** `POST`
- **Path:** `unread_entries.json`
- **Base URL:** `https://api.feedbin.com/v2`
- **Official documentation:** [Mark Entries Unread](https://github.com/feedbin/feedbin-api/blob/master/content/unread-entries.md#create-unread-entries-mark-as-unread)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `unread_entries` | body | `number<number>` | yes | Entry IDs to mark unread. Feedbin allows up to 1,000 IDs per request. Send multiple values as a array. |

# Mark Entries Read with Feedbin

Marks entries as read in Feedbin.

## Endpoint

- **Method:** `DELETE`
- **Path:** `unread_entries.json`
- **Base URL:** `https://api.feedbin.com/v2`
- **Official documentation:** [Mark Entries Read](https://github.com/feedbin/feedbin-api/blob/master/content/unread-entries.md#delete-unread-entries-mark-as-read)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `unread_entries` | body | `number<number>` | yes | Entry IDs to mark read. Feedbin allows up to 1,000 IDs per request. Send multiple values as a array. |

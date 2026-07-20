# Star Entries with Feedbin

Marks entries as starred in Feedbin.

## Endpoint

- **Method:** `POST`
- **Path:** `starred_entries.json`
- **Base URL:** `https://api.feedbin.com/v2`
- **Official documentation:** [Star Entries](https://github.com/feedbin/feedbin-api/blob/master/content/starred-entries.md#create-starred-entries)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `starred_entries` | body | `number<number>` | yes | Entry IDs to star. Feedbin allows up to 1,000 IDs per request. Send multiple values as a array. |

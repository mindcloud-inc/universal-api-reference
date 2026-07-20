# Unstar Entries with Feedbin

Removes starred status from entries in Feedbin.

## Endpoint

- **Method:** `DELETE`
- **Path:** `starred_entries.json`
- **Base URL:** `https://api.feedbin.com/v2`
- **Official documentation:** [Unstar Entries](https://github.com/feedbin/feedbin-api/blob/master/content/starred-entries.md#delete-starred-entries-unstar)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `starred_entries` | body | `number<number>` | yes | Entry IDs to unstar. Feedbin allows up to 1,000 IDs per request. Send multiple values as a array. |

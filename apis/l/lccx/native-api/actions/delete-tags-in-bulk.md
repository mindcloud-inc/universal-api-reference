# Delete Tags in Bulk with lc.cx

Deletes tags in bulk from lc.cx.

## Endpoint

- **Method:** `POST`
- **Path:** `/tags/delete/bulk`
- **Base URL:** `https://api.lc.cx/v1`
- **Official documentation:** [Delete Tags in Bulk](https://dev.lc.cx)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tags[]` | body | `array<string>` | yes | An array of tag IDs to delete. |

# Bulk Create Email List Records with Toofr

Creates multiple email list records in Toofr.

## Endpoint

- **Method:** `POST`
- **Path:** `/lists/:list_id/list_records/bulk_list_records`
- **Base URL:** `https://www.findemails.com/api/v1`
- **Official documentation:** [Bulk Create Email List Records](https://developer.findemails.com/?from=explinks.com)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `list_id` | path | `string` | yes | Email list ID. |
| `records` | query | `string` | yes | JSON array or encoded records payload to bulk create. |

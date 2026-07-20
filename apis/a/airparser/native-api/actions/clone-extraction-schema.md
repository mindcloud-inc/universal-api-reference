# Clone Extraction Schema with Airparser

Clones an extraction schema between Airparser inboxes.

## Endpoint

- **Method:** `POST`
- **Path:** `/inboxes/:inbox_id/schema-clone`
- **Base URL:** `https://api.airparser.com`
- **Official documentation:** [Clone Extraction Schema](https://help.airparser.com/public-api/public-api)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `inbox_id` | path | `string` | yes | The source Airparser inbox ID. |
| `destination_inbox_id` | body | `string` | yes | The destination inbox ID. |

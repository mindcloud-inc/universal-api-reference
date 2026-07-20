# Create Or Update Extraction Schema with Airparser

Creates or updates an extraction schema in Airparser.

## Endpoint

- **Method:** `POST`
- **Path:** `/inboxes/:inbox_id/schema`
- **Base URL:** `https://api.airparser.com`
- **Official documentation:** [Create Or Update Extraction Schema](https://help.airparser.com/public-api/public-api)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `inbox_id` | path | `string` | yes | The Airparser inbox ID. |
| `fields` | body | `list<object>` | yes | Array of extraction schema field definitions. |

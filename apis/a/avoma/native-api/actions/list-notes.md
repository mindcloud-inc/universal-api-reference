# List Notes with Avoma

Retrieves notes from Avoma.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/notes/`
- **Base URL:** `https://api.avoma.com`
- **Official documentation:** [List Notes](https://dev.avoma.com)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `from_date` | query | `string` | yes | Retrieve notes for meetings started at or after this UTC datetime. Use ISO 8601. |
| `to_date` | query | `string` | yes | Retrieve notes for meetings started at or before this UTC datetime. Use ISO 8601. |
| `page_size` | query | `number` | no | Number of records returned per response. |
| `output_format` | query | `string` | no | Format of notes to return: json, html, or markdown. |
| `meeting_uuid` | query | `string` | no | Unique ID of the meeting for which notes will be fetched. |
| `custom_category` | query | `string` | no | Unique ID of the custom category to filter notes by. |

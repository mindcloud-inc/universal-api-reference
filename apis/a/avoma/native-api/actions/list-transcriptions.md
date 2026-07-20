# List Transcriptions with Avoma

Retrieves transcriptions from Avoma.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/transcriptions/`
- **Base URL:** `https://api.avoma.com`
- **Official documentation:** [List Transcriptions](https://dev.avoma.com)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `from_date` | query | `string` | yes | Retrieve transcriptions for meetings started at or after this UTC datetime. Use ISO 8601 unless meeting UUID is provided. |
| `to_date` | query | `string` | yes | Retrieve transcriptions for meetings started at or before this UTC datetime. Use ISO 8601 unless meeting UUID is provided. |
| `meeting_uuid` | query | `string` | no | Unique ID of the meeting for which transcriptions will be fetched. |
| `page` | query | `number` | no | Page number for pagination when meeting UUID is not provided. |
| `page_size` | query | `number` | no | Number of items per page when meeting UUID is not provided. |

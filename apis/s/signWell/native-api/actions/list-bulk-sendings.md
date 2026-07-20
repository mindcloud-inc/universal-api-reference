# List Bulk Sendings with SignWell

Lists bulk sends available in SignWell.

## Endpoint

- **Method:** `GET`
- **Path:** `/bulk_sends`
- **Base URL:** `https://www.signwell.com/api/v1`
- **Official documentation:** [List Bulk Sendings](https://developers.signwell.com/reference/get_api-v1-bulk-sends)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `user_email` | query | `string` | no | Email address of the user that sent the Bulk Send. |
| `limit` | query | `number` | no | Number of documents to fetch. Defaults to 10, max is 50. |
| `page` | query | `number` | no | Page number for pagination. |
| `api_application_id` | query | `string` | no | Unique identifier for API Application settings to use. |

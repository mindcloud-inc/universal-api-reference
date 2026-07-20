# List Signature Activities with Skribble Sign

Retrieves signature activities from Skribble Sign.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/activities/signatures`
- **Base URL:** `https://api.skribble.com`
- **Official documentation:** [List Signature Activities](https://api-doc.skribble.com/#f2f445ee-c62b-4b0f-99ab-63ea72c2ba16)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `start_date` | query | `string` | yes | Start of the activity date range in yyyy-MM-dd format. |
| `end_date` | query | `string` | yes | End of the activity date range in yyyy-MM-dd format. |
| `page` | query | `number` | no | Page number starting at 1. |
| `size` | query | `number` | no | Number of activities to return per page. |
| `sort` | query | `string` | no | Sort order, such as asc or desc. |

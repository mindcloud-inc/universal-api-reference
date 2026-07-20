# Get People Report with Float

Retrieves a people report from Float.

## Endpoint

- **Method:** `GET`
- **Path:** `/reports/people`
- **Base URL:** `https://api.float.com/v3`
- **Official documentation:** [Get People Report](https://developer.float.com/api_reference.html#Reports)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `start_date` | query | `string` | yes | Start date of the report duration in the format YYYY-MM-DD |
| `end_date` | query | `string` | yes | End date of the report duration in the format YYYY-MM-DD |
| `people_id` | query | `number` | no | A people ID to filter the response on |

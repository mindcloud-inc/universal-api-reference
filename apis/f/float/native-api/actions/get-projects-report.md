# Get Projects Report with Float

Retrieves a projects report from Float.

## Endpoint

- **Method:** `GET`
- **Path:** `/reports/projects`
- **Base URL:** `https://api.float.com/v3`
- **Official documentation:** [Get Projects Report](https://developer.float.com/api_reference.html#Reports)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `start_date` | query | `string` | yes | Start date of the report duration in the format YYYY-MM-DD |
| `end_date` | query | `string` | yes | End date of the report duration in the format YYYY-MM-DD |
| `project_id` | query | `number` | no | A project ID to filter the response on |

# List Comments with SmartSuite

Retrieves comments from SmartSuite.

## Endpoint

- **Method:** `GET`
- **Path:** `/comments/`
- **Base URL:** `https://app.smartsuite.com/api/v1`
- **Official documentation:** [List Comments](https://developers.smartsuite.com/docs/solution-data/comments/list-comments)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `record` | query | `string` | yes | The SmartSuite record ID to list comments for. |
| `application` | query | `string` | no | Optional SmartSuite table ID filter. |
| `solution` | query | `string` | no | Optional SmartSuite solution ID filter. |

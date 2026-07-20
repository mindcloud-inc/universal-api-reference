# List API Connector Errors with Feathery

## Endpoint

- **Method:** `GET`
- **Path:** `/api/logs/api-connector/:form_id/`
- **Base URL:** `https://api.feathery.io`
- **Official documentation:** [List API Connector Errors](https://api-docs.feathery.io/#list-api-connector-errors)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `form_id` | path | `string` | yes | The ID of the form whose API connector errors you want to inspect. |
| `start_time` | query | `date` | no | Only return errors after this time. |
| `end_time` | query | `date` | no | Only return errors before this time. |

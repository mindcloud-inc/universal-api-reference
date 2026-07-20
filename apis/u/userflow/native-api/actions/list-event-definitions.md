# List Event Definitions with Userflow

Retrieves a list of event definitions from Userflow.

## Endpoint

- **Method:** `GET`
- **Path:** `/event_definitions`
- **Base URL:** `https://api.userflow.com`
- **Official documentation:** [List Event Definitions](https://docs.userflow.com/docs/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | query | `number` | no | Maximum number of event definitions to return. |
| `order_by` | query | `string` | no | Sort event definitions by created_at, display_name, or name. |
| `starting_after` | query | `string` | no | Return event definitions after this definition ID. |

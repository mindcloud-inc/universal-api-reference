# List Attribute Definitions with Userflow

Retrieves a list of attribute definitions from Userflow.

## Endpoint

- **Method:** `GET`
- **Path:** `/attribute_definitions`
- **Base URL:** `https://api.userflow.com`
- **Official documentation:** [List Attribute Definitions](https://docs.userflow.com/docs/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | query | `number` | no | Maximum number of attribute definitions to return. |
| `order_by` | query | `string` | no | Sort attribute definitions by created_at, display_name, or name. |
| `scope` | query | `string` | no | Filter attribute definitions by scope. |
| `starting_after` | query | `string` | no | Return attribute definitions after this definition ID. |

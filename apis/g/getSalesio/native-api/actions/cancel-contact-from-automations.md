# Cancel Contact From Automations with GetSales.io

## Endpoint

- **Method:** `PUT`
- **Path:** `/flows/api/flows/leads/{leadUuid}/cancel`
- **Base URL:** `https://amazing.getsales.io`
- **Official documentation:** [Cancel Contact From Automations](https://api.getsales.io/api/openapi/automations/cancelleadfromflows.md)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `leadUuid` | path | `string` | yes | UUID of the contact to cancel from selected automations. |
| `flow_uuids[]` | body | `array<string>` | yes | Array of automation UUIDs to cancel the contact from. |

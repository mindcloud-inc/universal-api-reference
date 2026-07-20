# Cancel Contact From All Automations with GetSales.io

## Endpoint

- **Method:** `PUT`
- **Path:** `/flows/api/flows/leads/{leadUuid}/cancel-all`
- **Base URL:** `https://amazing.getsales.io`
- **Official documentation:** [Cancel Contact From All Automations](https://api.getsales.io/api/openapi/automations/cancelleadfromallflows.md)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `leadUuid` | path | `string` | yes | UUID of the contact to cancel from all active automations. |

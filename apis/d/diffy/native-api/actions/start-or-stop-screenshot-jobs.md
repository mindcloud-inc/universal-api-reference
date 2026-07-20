# Start or Stop Screenshot Jobs with Diffy

Starts or stops screenshot jobs in Diffy.

## Endpoint

- **Method:** `PUT`
- **Path:** `/snapshots/:id/:action`
- **Base URL:** `https://app.diffy.website/api`
- **Official documentation:** [Start or Stop Screenshot Jobs](https://app.diffy.website/rest)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `action` | path | `string` | no | Job control action: start or stop. |
| `id` | path | `number` | yes | Screenshot ID. |

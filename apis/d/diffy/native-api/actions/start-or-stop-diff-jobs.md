# Start or Stop Diff Jobs with Diffy

Starts or stops diff jobs in Diffy.

## Endpoint

- **Method:** `PUT`
- **Path:** `/diffs/:id/:action`
- **Base URL:** `https://app.diffy.website/api`
- **Official documentation:** [Start or Stop Diff Jobs](https://app.diffy.website/rest)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `action` | path | `string` | no | Job control action: start or stop. |
| `id` | path | `number` | yes | Diff ID. |

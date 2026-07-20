# Get Status with Quire

Retrieves a status from a Quire project.

## Endpoint

- **Method:** `GET`
- **Path:** `status/id/:projectId/:value`
- **Base URL:** `https://quire.io/api`
- **Official documentation:** [Get Status](https://quire.io/dev/api/#operation--status-id--projectId---value--get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | Project ID. |
| `value` | path | `number` | yes | Status value to fetch. |

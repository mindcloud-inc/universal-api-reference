# Update Assignment with Previsto

Updates an existing assignment in Previsto.

## Endpoint

- **Method:** `PUT`
- **Path:** `/assignments/:id`
- **Base URL:** `https://api.previsto.io`
- **Official documentation:** [Update Assignment](https://developer.previsto.com/assignments/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Previsto assignment ID. |
| `accountId` | body | `string` | no | Assigned worker account ID. |

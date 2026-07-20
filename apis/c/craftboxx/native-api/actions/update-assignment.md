# Update Assignment with Craftboxx

Updates an assignment in Craftboxx.

## Endpoint

- **Method:** `PUT`
- **Path:** `assignments/:assignmentId`
- **Base URL:** `https://api.craftboxx.de`
- **Official documentation:** [Update Assignment](https://api.craftboxx.de/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `assignmentId` | path | `number` | yes | The Craftboxx assignment ID. |
| `end` | body | `string` | no | The assignment end timestamp. |
| `start` | body | `string` | no | The assignment start timestamp. |
| `state` | body | `string` | no | The assignment state. |
| `title` | body | `string` | no | The assignment title. |

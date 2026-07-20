# List Webhooks Configuration with Localazy

Retrieves webhook endpoints from a Localazy project.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/:projectId/webhooks`
- **Base URL:** `https://api.localazy.com`
- **Official documentation:** [List Webhooks Configuration](https://localazy.com/docs/api/webhooks-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | Localazy project identifier or slug. |

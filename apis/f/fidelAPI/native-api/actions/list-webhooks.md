# List Webhooks with Fidel API

Retrieves webhooks from a Fidel program.

## Endpoint

- **Method:** `GET`
- **Path:** `/programs/:programId/hooks`
- **Base URL:** `https://api.fidel.uk/v1`
- **Official documentation:** [List Webhooks](https://reference.fidel.uk/reference/list-webhooks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `programId` | path | `string` | yes | — |
| `event` | query | `string` | no | Filter webhooks by event name. |

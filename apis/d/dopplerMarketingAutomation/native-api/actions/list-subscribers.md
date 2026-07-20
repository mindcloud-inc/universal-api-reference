# List Subscribers with Doppler Marketing Automation

Retrieves subscribers from a Doppler Marketing Automation list.

## Endpoint

- **Method:** `GET`
- **Path:** `/accounts/:accountName/lists/:listId/subscribers`
- **Base URL:** `https://restapi.fromdoppler.com`
- **Official documentation:** [List Subscribers](https://restapi.fromdoppler.com/docs/rels/get-subscriber-collection)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `listId` | path | `string` | yes | Doppler list identifier. |

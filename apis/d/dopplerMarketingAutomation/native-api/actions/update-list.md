# Update List with Doppler Marketing Automation

Updates an existing list in Doppler Marketing Automation.

## Endpoint

- **Method:** `PUT`
- **Path:** `/accounts/:accountName/lists/:listId`
- **Base URL:** `https://restapi.fromdoppler.com`
- **Official documentation:** [Update List](https://restapi.fromdoppler.com/docs/rels/edit-list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `listId` | path | `string` | yes | Doppler list identifier. |
| `name` | body | `string` | yes | Updated name for the Doppler list. |

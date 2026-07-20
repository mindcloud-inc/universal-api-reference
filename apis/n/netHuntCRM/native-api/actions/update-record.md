# Update Record with NetHunt CRM

Updates an existing record in NetHunt CRM.

## Endpoint

- **Method:** `POST`
- **Path:** `/actions/update-record/:recordId`
- **Base URL:** `https://nethunt.com/api/v1/zapier`
- **Official documentation:** [Update Record](https://nethunt.com/integration-api#update-record)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fieldActions` | body | `object` | yes | Field actions payload keyed by NetHunt field name, with add/remove/overwrite instructions. |
| `overwrite` | query | `boolean` | no | Default overwrite setting for field actions. |
| `recordId` | path | `string` | yes | Record ID to update. |

# Add Campaign Connection with TxtSync

Adds recipients to a campaign in TxtSync.

## Endpoint

- **Method:** `POST`
- **Path:** `/campaigns/:id/connections`
- **Base URL:** `https://api.txtsync.com`
- **Official documentation:** [Add Campaign Connection](https://docs.txtsync.com/#add-campaign-connection)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | — |
| `ContactIDs` | body | `list<number>` | no | Send multiple values as a array. |
| `TagIDs` | body | `list<number>` | no | Send multiple values as a array. |
| `Numbers` | body | `list<string>` | no | Send multiple values as a array. |

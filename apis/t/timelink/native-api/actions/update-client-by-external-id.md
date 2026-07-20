# Update Client by External ID with Timelink

Updates an existing client in Timelink by external ID.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/clients/ext/:extId`
- **Base URL:** `https://api.timelink.io/api/v1`
- **Official documentation:** [Update Client by External ID](https://api.timelink.io/documentation#/Clients/patch_api_v1_clients_ext__ext-id_)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `extId` | path | `string` | yes | The external reference ID for the client. |
| `name` | body | `string` | no | Updated client name. |
| `active` | body | `boolean` | no | Whether the client remains active. |

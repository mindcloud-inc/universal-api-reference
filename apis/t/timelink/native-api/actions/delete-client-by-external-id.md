# Delete Client by External ID with Timelink

Deletes an existing client from Timelink by external ID.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/clients/ext/:extId`
- **Base URL:** `https://api.timelink.io/api/v1`
- **Official documentation:** [Delete Client by External ID](https://api.timelink.io/documentation#/Clients/delete_api_v1_clients_ext__ext-id_)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `extId` | path | `string` | yes | The external reference ID for the client. |

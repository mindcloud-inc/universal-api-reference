# Create Transfer with smsmode

## Endpoint

- **Method:** `POST`
- **Path:** `commons/v1/organisations/:organisationId/transfers`
- **Base URL:** `https://rest.smsmode.com/`
- **Official documentation:** [Create Transfer](https://dev.smsmode.com/commons/v1/#tag/Transfer/operation/transfer-creation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organisationId` | path | `string` | yes | Organisation ID path parameter from the smsmode API route. |
| `organisationDestination` | body | `object` | yes | Destination Organisation request body field documented by the smsmode API. |
| `amount` | body | `number` | yes | Amount request body field documented by the smsmode API. |
| `reference` | body | `string` | no | Reference request body field documented by the smsmode API. |
| `description` | body | `string` | no | Description request body field documented by the smsmode API. |

# Cancel Order with PostcardMania

Cancels an existing order in PostcardMania.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/order/{{orderID}}`
- **Base URL:** `https://v3.pcmintegrations.com`
- **Official documentation:** [Cancel Order](https://docs.pcmintegrations.com/docs/directmail-api/iuc7kuzptpgwv)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `orderID` | path | `string` | no | The order identifier to delete. |

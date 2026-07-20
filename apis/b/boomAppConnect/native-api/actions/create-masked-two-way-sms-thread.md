# Create Masked Two-Way SMS Thread with boomApp Connect

Creates a masked two-way SMS thread in boomApp Connect.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/maskTwoWay`
- **Base URL:** `https://direct-api.apps.boomcomms.com`
- **Official documentation:** [Create Masked Two-Way SMS Thread](https://github.com/microsoft/PowerPlatformConnectors/blob/dev/certified-connectors/BoomappConnect/apiDefinition.swagger.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `from` | body | `string` | yes | Sender number for the masked two-way thread. Required for successful runtime submission. |
| `to` | body | `string` | yes | Recipient number for the masked two-way thread. Required for successful runtime submission. |
| `reference` | body | `string` | yes | Reference value for the masked two-way thread. Required for successful runtime submission. |
| `reference_always` | body | `boolean` | no | Whether the reference should always be included. |
| `rounds` | body | `number` | no | Number of conversation rounds. |
| `validity` | body | `number` | no | Thread validity period. |
| `message` | body | `string` | yes | Initial message for the masked two-way thread. Required for successful runtime submission. |

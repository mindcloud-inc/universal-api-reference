# Update Etch Packet with Anvil

Updates an existing Etch packet in Anvil.

## Endpoint

- **Method:** `POST`
- **Path:** `/`
- **Base URL:** `https://graphql.useanvil.com`
- **Official documentation:** [Update Etch Packet](https://www.useanvil.com/docs/api/graphql/reference/#mutation-updateEtchPacket)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variables.eid` | body | `string` | yes | Provide EID for Update Etch Packet. |
| `variables.token` | body | `string` | no | Provide Token for Update Etch Packet. |
| `variables.isArchived` | body | `boolean` | no | Provide Is Archived for Update Etch Packet. |
| `variables.name` | body | `string` | no | Provide Name for Update Etch Packet. |
| `variables.webhookURL` | body | `string` | no | Provide Webhook URL for Update Etch Packet. |
| `variables.payload` | body | `object` | no | Provide Payload for Update Etch Packet. |
| `variables.mergePayloads` | body | `boolean` | no | Provide Merge Payloads for Update Etch Packet. |

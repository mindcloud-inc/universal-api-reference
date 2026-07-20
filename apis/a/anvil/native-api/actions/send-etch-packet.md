# Send Etch Packet with Anvil

Sends or resends an Etch packet in Anvil.

## Endpoint

- **Method:** `POST`
- **Path:** `/`
- **Base URL:** `https://graphql.useanvil.com`
- **Official documentation:** [Send Etch Packet](https://www.useanvil.com/docs/api/graphql/reference/#mutation-sendEtchPacket)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variables.eid` | body | `string` | yes | Provide EID for Send Etch Packet. |

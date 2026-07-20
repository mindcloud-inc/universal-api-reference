# Get Key Quorum with Privy

Retrieves a key quorum from Privy.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/key_quorums/{{keyQuorumId}}`
- **Base URL:** `https://api.privy.io`
- **Official documentation:** [Get Key Quorum](https://api.privy.io/v1/openapi.json#/paths/~1v1~1key_quorums~1{key_quorum_id}/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `key_quorum_id` | path | `string` | yes | Privy key quorum ID. |

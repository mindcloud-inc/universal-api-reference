# Get Address Sequence with Overledger

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/autoexecution/search/address/sequence/:addressId`
- **Base URL:** `https://api.overledger.dev`
- **Official documentation:** [Get Address Sequence](https://docs.overledger.dev/docs/address-sequence)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `addressId` | path | `string` | yes | Blockchain address whose sequence/nonce should be retrieved. |
| `location` | body | `object` | yes | Overledger location object with technology and network. |

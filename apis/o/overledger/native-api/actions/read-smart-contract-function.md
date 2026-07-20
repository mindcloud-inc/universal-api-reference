# Read Smart Contract Function with Overledger

## Endpoint

- **Method:** `POST`
- **Path:** `/api/smart-contracts/read`
- **Base URL:** `https://api.overledger.dev`
- **Official documentation:** [Read Smart Contract Function](https://docs.overledger.dev/docs/read)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `API-Version` | `3.0.0` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `location` | body | `object` | yes | Overledger location object with technology and network. |
| `functionName` | body | `string` | yes | Smart contract read function name. |
| `smartContractId` | body | `string` | yes | Smart contract identifier/address. |
| `inputParameters[]` | body | `array<object>` | no | Optional array of smart contract input parameter objects with type and value. |
| `outputParameters[]` | body | `array<object>` | no | Optional array of smart contract output parameter objects with type. |

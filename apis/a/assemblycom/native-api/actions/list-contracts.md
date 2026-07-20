# List Contracts with Assembly.com

Retrieves contracts from Assembly.com.

## Endpoint

- **Method:** `GET`
- **Path:** `/contracts`
- **Base URL:** `https://api.assembly.com/v1`
- **Official documentation:** [List Contracts](https://docs.assembly.com/reference/list-contracts)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contractTemplateId` | query | `string` | no | The unique ID of the contract template the contract is associated with. |
| `status` | query | `string` | no | The current state of the contract. Options are pending or signed. Accepted values: `0`, `1`. |
| `clientId` | query | `string` | no | The ID of the client that the contract was sent to. |

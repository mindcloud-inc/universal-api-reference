# Send Contract with Assembly.com

Sends a contract in Assembly.com.

## Endpoint

- **Method:** `POST`
- **Path:** `/contracts`
- **Base URL:** `https://api.assembly.com/v1`
- **Official documentation:** [Send Contract](https://docs.assembly.com/reference/send-contract)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contractTemplateId` | body | `string` | yes | The unique ID of the contract template the contract is associated with. |
| `clientId` | body | `string` | yes | The unique ID of the client receiving the contract request. |
| `companyId` | body | `string` | no | The company ID of the client. Required when the client has more than one company. |
| `variableValues` | body | `string` | no | A list of fields which represent the specific values for certain contract inputs. |

# Update Signer with Anvil

Updates an existing signer in Anvil.

## Endpoint

- **Method:** `POST`
- **Path:** `/`
- **Base URL:** `https://graphql.useanvil.com`
- **Official documentation:** [Update Signer](https://www.useanvil.com/docs/api/graphql/reference/#mutation-updateSigner)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variables.eid` | body | `string` | yes | Provide EID for Update Signer. |
| `variables.name` | body | `string` | no | Provide Name for Update Signer. |
| `variables.email` | body | `string` | no | Provide Email for Update Signer. |
| `variables.aliasId` | body | `string` | no | Provide Alias ID for Update Signer. |
| `variables.activateIfPending` | body | `boolean` | no | Provide Activate If Pending for Update Signer. |

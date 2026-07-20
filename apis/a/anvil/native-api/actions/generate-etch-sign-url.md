# Generate Etch Sign URL with Anvil

Generates an embedded signing URL in Anvil.

## Endpoint

- **Method:** `POST`
- **Path:** `/`
- **Base URL:** `https://graphql.useanvil.com`
- **Official documentation:** [Generate Etch Sign URL](https://www.useanvil.com/docs/api/graphql/reference/#mutation-generateEtchSignURL)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variables.signerEid` | body | `string` | yes | Provide Signer EID for Generate Etch Sign URL. |
| `variables.clientUserId` | body | `string` | yes | Provide Client User ID for Generate Etch Sign URL. |

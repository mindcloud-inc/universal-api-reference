# Skip Signer with Anvil

Skips an existing signer in Anvil.

## Endpoint

- **Method:** `POST`
- **Path:** `/`
- **Base URL:** `https://graphql.useanvil.com`
- **Official documentation:** [Skip Signer](https://www.useanvil.com/docs/api/graphql/reference/#mutation-skipSigner)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variables.signerEid` | body | `string` | yes | Provide Signer EID for Skip Signer. |
| `variables.clearNameAndEmail` | body | `boolean` | no | Provide Clear Name And Email for Skip Signer. |

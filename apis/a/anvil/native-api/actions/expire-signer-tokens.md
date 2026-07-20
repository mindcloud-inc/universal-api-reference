# Expire Signer Tokens with Anvil

Expires a signer's active tokens in Anvil.

## Endpoint

- **Method:** `POST`
- **Path:** `/`
- **Base URL:** `https://graphql.useanvil.com`
- **Official documentation:** [Expire Signer Tokens](https://www.useanvil.com/docs/api/graphql/reference/#mutation-expireSignerTokens)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variables.signerEid` | body | `string` | yes | Provide Signer EID for Expire Signer Tokens. |

# Resolve Account Identifier with OpenSea

Resolves an OpenSea account identifier.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/accounts/resolve/{identifier}`
- **Base URL:** `https://api.opensea.io`
- **Official documentation:** [Resolve Account Identifier](https://docs.opensea.io/reference/resolve_account)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `identifier` | path | `string` | yes | An ENS name (e.g. vitalik.eth), OpenSea username, or wallet address to resolve |

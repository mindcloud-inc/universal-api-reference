# List Documents with Basecamp

Retrieves documents from a Basecamp vault.

## Endpoint

- **Method:** `GET`
- **Path:** `/:accountId/vaults/:vaultId/documents.json`
- **Base URL:** `https://3.basecampapi.com`
- **Official documentation:** [List Documents](https://github.com/basecamp/bc3-api/blob/master/sections/documents.md#get-documents)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `accountId` | path | `string` | yes |
| `vaultId` | path | `number` | yes |

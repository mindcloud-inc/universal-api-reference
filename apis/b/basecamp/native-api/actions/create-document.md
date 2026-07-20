# Create Document with Basecamp

Creates a new document in a Basecamp vault.

## Endpoint

- **Method:** `POST`
- **Path:** `/:accountId/vaults/:vaultId/documents.json`
- **Base URL:** `https://3.basecampapi.com`
- **Official documentation:** [Create Document](https://github.com/basecamp/bc3-api/blob/master/sections/documents.md#create-a-document)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `accountId` | path | `string` | yes |
| `vaultId` | path | `number` | yes |
| `title` | body | `string` | yes |
| `content` | body | `string` | yes |
| `status` | body | `string` | no |

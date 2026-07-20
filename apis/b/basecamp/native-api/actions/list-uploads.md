# List Uploads with Basecamp

Retrieves uploads from a Basecamp vault.

## Endpoint

- **Method:** `GET`
- **Path:** `/:accountId/vaults/:vaultId/uploads.json`
- **Base URL:** `https://3.basecampapi.com`
- **Official documentation:** [List Uploads](https://github.com/basecamp/bc3-api/blob/master/sections/uploads.md#get-uploads)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `accountId` | path | `string` | yes |
| `vaultId` | path | `number` | yes |

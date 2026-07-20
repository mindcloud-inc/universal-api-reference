# Search Documents with SignRequest

## Endpoint

- **Method:** `GET`
- **Path:** `/documents-search/`
- **Base URL:** `https://signrequest.com/api/v1`
- **Official documentation:** [Search Documents](https://signrequest.com/api/v1/docs/#operation/documents-search_list)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `q` | query | `string` | no | Normal search query |
| `autocomplete` | query | `string` | no | Partial search query |
| `name` | query | `string` | no | Document name |
| `subdomain` | query | `string` | no | Send multiple values as a string separated by `\|`. |
| `signer_emails` | query | `string` | no | Email needed to sign or approve Send multiple values as a string separated by `\|`. |
| `status` | query | `list<string>` | no | Document status filter Accepted values: `ca`, `co`, `de`, `do`, `ec`, `es`, `ne`, `sd`, `se`, `si`, `vi`, `xp`. Send multiple values as a string separated by `\|`. |
| `who` | query | `list<string>` | no | Signer participation filter Accepted values: `m`, `mo`, `o`. Send multiple values as a string separated by `\|`. |
| `format` | query | `list<string>` | no | Export format Accepted values: `csv`, `json`, `xls`. |
| `signer_data` | query | `number` | no | Set to 1 to export each signer on a separate row |

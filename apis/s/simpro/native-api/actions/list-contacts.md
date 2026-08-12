# List Contacts with Simpro

## Endpoint

- **Method:** `GET`
- **Path:** `/companies/:companyId/contacts/`
- **Base URL:** `{buildUrl}/api/v1.0`
- **Official documentation:** [List Contacts](https://developer.simprogroup.com/apidoc/?page=9aa698f602b1e5694855cee73a683488)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `companyId` | path | `number` | yes | Simpro company ID. Single-company builds usually use 0. |
| `pageSize` | query | `number` | no | Maximum contacts per page. |
| `page` | query | `number` | no | Page number. |
| `limit` | query | `number` | no | Hard limit for number of results. |
| `columns[]` | query | `array<string>` | no | Columns to return for each contact. |

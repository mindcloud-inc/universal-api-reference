# List Legal Notices with iubenda

Retrieves legal notices from iubenda.

## Endpoint

- **Method:** `GET`
- **Path:** `/legal_notices`
- **Base URL:** `https://consent.iubenda.com`
- **Official documentation:** [List Legal Notices](https://www.iubenda.com/en/help/6484-consent-solution-http-api-documentation/#legal-notices)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `identifier` | query | `string` | no | Filter by an exact legal notice identifier. |
| `version` | query | `number` | no | Filter by an exact legal notice version. |
| `language` | query | `string` | no | Filter legal notices by content language such as en or it. |
| `id` | query | `string` | no | Filter by an exact legal notice ID. |
| `from_time` | query | `string` | no | Return legal notices from this timestamp onward. |
| `to_time` | query | `string` | no | Return legal notices up to this timestamp. |
| `starting_after_identifier` | query | `string` | no | Cursor identifier component for legal notice pagination. |
| `starting_after_version` | query | `number` | no | Cursor version component for legal notice pagination. |
| `limit` | query | `number` | no | Maximum number of legal notices to return. |

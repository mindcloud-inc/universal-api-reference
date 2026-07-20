# List Legal Notice Versions with iubenda

Retrieves legal notice versions from iubenda.

## Endpoint

- **Method:** `GET`
- **Path:** `/legal_notices/:identifier`
- **Base URL:** `https://consent.iubenda.com`
- **Official documentation:** [List Legal Notice Versions](https://www.iubenda.com/en/help/6484-consent-solution-http-api-documentation/#legal-notices)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `identifier` | path | `string` | yes | Identifier of the legal notice |
| `limit` | query | `number` | no | Maximum number of legal notice versions to return. |
| `starting_after` | query | `number` | no | Cursor for pagination across legal notice versions. |

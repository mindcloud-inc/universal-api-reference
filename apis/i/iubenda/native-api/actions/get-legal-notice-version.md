# Get Legal Notice Version with iubenda

Retrieves a legal notice version from iubenda.

## Endpoint

- **Method:** `GET`
- **Path:** `/legal_notices/:identifier/:version`
- **Base URL:** `https://consent.iubenda.com`
- **Official documentation:** [Get Legal Notice Version](https://www.iubenda.com/en/help/6484-consent-solution-http-api-documentation/#legal-notices)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `identifier` | path | `string` | yes | Identifier of the legal notice |
| `version` | path | `number` | yes | Version of the legal notice |

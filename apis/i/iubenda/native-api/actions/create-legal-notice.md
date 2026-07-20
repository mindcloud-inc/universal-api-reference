# Create Legal Notice with iubenda

Creates a legal notice in iubenda.

## Endpoint

- **Method:** `POST`
- **Path:** `/legal_notices`
- **Base URL:** `https://consent.iubenda.com`
- **Official documentation:** [Create Legal Notice](https://www.iubenda.com/en/help/6484-consent-solution-http-api-documentation/#legal-notices)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `identifier` | body | `string` | yes | Stable legal notice identifier. |
| `content` | body | `string` | yes | Legal notice content, as a string or language-keyed object. |
| `timestamp` | body | `string` | no | Legal notice timestamp. |
| `document_ids[]` | body | `array<string>` | no | Document IDs associated with the legal notice. |

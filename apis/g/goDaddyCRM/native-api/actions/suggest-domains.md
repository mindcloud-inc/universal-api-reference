# Suggest Domains with GoDaddy CRM

Suggests domains with the GoDaddy API.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/domains/suggest`
- **Base URL:** `https://api.godaddy.com`
- **Official documentation:** [Suggest Domains](https://developer.godaddy.com/doc/endpoint/domains)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | query | `string` | no | Domain name or keywords for which alternative domains will be suggested. |
| `country` | query | `string` | no | Two-letter ISO country code used as a target region hint. |
| `city` | query | `string` | no | City name used as a target region hint. |
| `sources[]` | query | `array<string>` | no | Suggestion sources to query. |
| `tlds[]` | query | `array<string>` | no | Top-level domains to include in suggestions. |
| `lengthMax` | query | `number` | no | Maximum length of the second-level domain. |
| `lengthMin` | query | `number` | no | Minimum length of the second-level domain. |
| `limit` | query | `number` | no | Maximum number of suggestions to return. |
| `waitMs` | query | `number` | no | Maximum amount of time, in milliseconds, to wait for responses. |

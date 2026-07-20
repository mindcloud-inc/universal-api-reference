# Get Domain Keywords with Adyntel

Retrieves paid and organic keywords for a domain in Adyntel.

## Endpoint

- **Method:** `POST`
- **Path:** `/domain-keywords`
- **Base URL:** `https://api.adyntel.com`
- **Official documentation:** [Get Domain Keywords](https://docs.adyntel.com/ad-libraries/paid-vs-organic-keywords)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `company_domain` | body | `string` | yes | Company website without www or http. |
| `language` | body | `string` | no | Language for keyword results. |
| `limit` | body | `number` | no | Number of results to return. |

# Enrich a person or a company with Datagma

Retrieves person or company enrichment data from Datagma.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/full`
- **Base URL:** `https://gateway.datagma.net/api/ingress`
- **Official documentation:** [Enrich a person or a company](https://datagmaapi.readme.io/reference/ingressservice_fullapiv2)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data` | query | `string` | no | Primary enrichment input such as a company name, domain, website, SIREN number, LinkedIn URL, or email address. |
| `fullName` | query | `string` | no | Target person's full name when enriching a person. |
| `phoneFull` | query | `string` | no | Set true to find a mobile phone number from a full name and company name. |
| `companyPremium` | query | `string` | no | Include basic company information in the response. |
| `companyFull` | query | `string` | no | Include extended company information in the response. |
| `whatsappCheck` | query | `string` | no | Set true to verify whether a found number is linked to WhatsApp. |
| `debug` | query | `string` | no | Set false to allow broader scoring results; defaults to false. |

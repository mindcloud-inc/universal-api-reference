# Purchase Domain Privacy with GoDaddy CRM

Purchases domain privacy for a GoDaddy domain.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/domains/:domain/privacy/purchase`
- **Base URL:** `https://api.godaddy.com`
- **Official documentation:** [Purchase Domain Privacy](https://developer.godaddy.com/doc/endpoint/domains)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `domain` | path | `string` | yes | Required domain for the privacy purchase |
| `consent.agreementKeys[]` | body | `string<string>` | yes | Required agreement keys, including DNPA Send multiple values as a array. |
| `consent.agreedBy` | body | `string` | yes | Required IP address of the consenting end user |
| `consent.agreedAt` | body | `string` | yes | Required consent timestamp in ISO format |

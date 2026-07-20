# Add Client with Whautomate

Creates a new client in Whautomate.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/clients`
- **Base URL:** `https://api.whautomate.com`
- **Official documentation:** [Add Client](https://help.whautomate.com/product-guides/whautomate-rest-api/clients)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `contactType` | body | `string` | no |
| `countryCode` | body | `string` | no |
| `email` | body | `string` | no |
| `fullName` | body | `string` | yes |
| `phone` | body | `string` | no |
| `preferredName` | body | `string` | no |
| `primaryLocation` | body | `object` | yes |
| `tags[]` | body | `array<string>` | no |

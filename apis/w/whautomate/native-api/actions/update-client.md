# Update Client with Whautomate

Updates an existing client in Whautomate.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v1/clients/{{clientId}}`
- **Base URL:** `https://api.whautomate.com`
- **Official documentation:** [Update Client](https://help.whautomate.com/product-guides/whautomate-rest-api/clients)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `clientId` | path | `string` | yes |
| `contactType` | body | `string` | no |
| `countryCode` | body | `string` | no |
| `email` | body | `string` | no |
| `fullName` | body | `string` | no |
| `phone` | body | `string` | no |
| `preferredName` | body | `string` | no |
| `primaryLocation` | body | `object` | no |
| `tags[]` | body | `array<string>` | no |

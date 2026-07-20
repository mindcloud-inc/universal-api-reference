# Remove Tags from Client with Whautomate

Updates an existing client in Whautomate by removing tags.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/clients/{{clientId}}/tags/remove`
- **Base URL:** `https://api.whautomate.com`
- **Official documentation:** [Remove Tags from Client](https://help.whautomate.com/product-guides/whautomate-rest-api/clients)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `clientId` | path | `string` | yes |
| `tags[]` | body | `array<string>` | yes |

# Add Tags to Client with Whautomate

Updates an existing client in Whautomate by adding tags.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/clients/{{clientId}}/tags/add`
- **Base URL:** `https://api.whautomate.com`
- **Official documentation:** [Add Tags to Client](https://help.whautomate.com/product-guides/whautomate-rest-api/clients)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `clientId` | path | `string` | yes |
| `tags[]` | body | `array<string>` | yes |

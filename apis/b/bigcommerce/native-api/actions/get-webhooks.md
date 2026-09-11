# Get Webhooks with BigCommerce

## Endpoint

- **Method:** `GET`
- **Path:** `/v3/hooks`
- **Base URL:** `https://api.bigcommerce.com/stores/{storeHash}`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `scope` | body | `string` | yes | — |
| `destination` | body | `string` | yes | URL must be active, return a 200 response, and be served on port 443. Custom ports arenʼt currently supported. |
| `isActive` | body | `boolean` | no | Boolean value that indicates whether the webhook is active or not. A webhook subscription becomes deactivated after 90 days of inactivity. |
| `headers` | body | `object` | no | Headers used to validate that webhooks are active. You can pass in any number of custom headers to validate webhooks are being returned. |

# Create Customer with Vouchery.io

## Endpoint

- **Method:** `POST`
- **Path:** `/customers`
- **Base URL:** `https://mindcloud.sandbox.vouchery.app/api/v2.1`
- **Official documentation:** [Create Customer](https://docs.vouchery.io/reference/postapiv21customers)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `identifier` | body | `string` | yes | Unique customer identifier. |
| `name` | body | `string` | no | Customer name. |
| `email` | body | `string` | no | Customer email. |
| `loyalty_points` | body | `number` | no | Customer loyalty points. |
| `metadata` | body | `string` | yes | JSON object string for customer metadata. |
| `categories` | body | `string` | yes | JSON array string of category objects with tag and name. |
| `referrer_code` | body | `string` | no | Customer referrer code. |

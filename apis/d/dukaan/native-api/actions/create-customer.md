# Create Customer with Dukaan

Creates a new customer in Dukaan.

## Endpoint

- **Method:** `POST`
- **Path:** `api/campaign/seller/store-lead/v2/`
- **Base URL:** `https://api.mydukaan.io`
- **Official documentation:** [Create Customer](https://documenter.getpostman.com/view/25389466/2s9Yynk3f7)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Customer name. |
| `email` | body | `string` | no | Customer email address. |
| `mobile` | body | `string` | yes | Customer mobile number. |
| `store` | body | `number` | yes | Store ID for the customer. |

# Get Webhooks Admin Info with BigCommerce

## Endpoint

- **Method:** `GET`
- **Path:** `/v3/hooks/admin`
- **Base URL:** `https://api.bigcommerce.com/stores/{storeHash}`
- **Official documentation:** [Get Webhooks Admin Info](https://developer.bigcommerce.com/docs/webhooks/webhooks/webhooks-admin#get-admin-info)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `isActive` | query | `boolean` | no | Boolean value that indicates whether the webhook is active or not. A webhook subscription becomes deactivated after 90 days of inactivity. Format: `toggle`. |

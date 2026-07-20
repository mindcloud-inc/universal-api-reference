# List Fields For Checkout Page with Checkout Page

Retrieves fields for a checkout page in Checkout Page.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/checkout-pages/:pageId/fields`
- **Base URL:** `https://api.checkoutpage.com`
- **Official documentation:** [List Fields For Checkout Page](https://checkoutpage.com/docs/api/v1/checkout-pages/fields/list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `pageId` | path | `string` | yes | Unique identifier. Must be in BSON ObjectId format. |

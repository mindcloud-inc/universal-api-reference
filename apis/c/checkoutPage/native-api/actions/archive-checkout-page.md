# Archive Checkout Page with Checkout Page

Archives a checkout page in Checkout Page.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v1/checkout-pages/:pageId`
- **Base URL:** `https://api.checkoutpage.com`
- **Official documentation:** [Archive Checkout Page](https://checkoutpage.com/docs/api/v1/checkout-pages/delete)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `pageId` | path | `string` | yes | Unique identifier. Must be in BSON ObjectId format. |

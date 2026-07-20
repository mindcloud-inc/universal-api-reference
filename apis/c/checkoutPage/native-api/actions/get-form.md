# Get Form with Checkout Page

Retrieves a form from Checkout Page.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/forms/:pageId`
- **Base URL:** `https://api.checkoutpage.com`
- **Official documentation:** [Get Form](https://checkoutpage.com/docs/api/v1/forms/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `pageId` | path | `string` | yes | Unique identifier. Must be in BSON ObjectId format. |

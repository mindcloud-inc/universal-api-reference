# List Fields For Form with Checkout Page

Retrieves fields for a form in Checkout Page.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/forms/:pageId/fields`
- **Base URL:** `https://api.checkoutpage.com`
- **Official documentation:** [List Fields For Form](https://checkoutpage.com/docs/api/v1/forms/fields/list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `pageId` | path | `string` | yes | Unique identifier. Must be in BSON ObjectId format. |

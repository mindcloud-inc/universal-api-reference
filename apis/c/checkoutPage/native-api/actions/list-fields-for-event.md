# List Fields For Event with Checkout Page

Retrieves fields for an event in Checkout Page.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/events/:pageId/fields`
- **Base URL:** `https://api.checkoutpage.com`
- **Official documentation:** [List Fields For Event](https://checkoutpage.com/docs/api/v1/events/fields/list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `pageId` | path | `string` | yes | Unique identifier. Must be in BSON ObjectId format. |

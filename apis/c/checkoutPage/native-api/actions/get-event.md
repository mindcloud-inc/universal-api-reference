# Get Event with Checkout Page

Retrieves a event from Checkout Page.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/events/:pageId`
- **Base URL:** `https://api.checkoutpage.com`
- **Official documentation:** [Get Event](https://checkoutpage.com/docs/api/v1/events/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `pageId` | path | `string` | yes | Unique identifier. Must be in BSON ObjectId format. |

# Customize Event Landing Page with Airmeet

Updates an event landing page in Airmeet.

## Endpoint

- **Method:** `PUT`
- **Path:** `/airmeet/{airmeetId}/landing-page`
- **Base URL:** `https://api-gateway-prod.us.airmeet.com/prod`
- **Official documentation:** [Customize Event Landing Page](https://help.airmeet.com/support/solutions/articles/82000909770-3-manage-event-airmeet-public-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `airmeetId` | path | `string` | yes | The Airmeet event ID. |
| `ambience` | body | `string` | no | Landing page theme, LIGHT or DARK. |
| `buttonTextColor` | body | `string` | no | Hex color for button text, for example #ff9847. |
| `highlightColor` | body | `string` | no | Hex color for highlight elements, for example #0000ff. |
| `imageUrl` | body | `string` | no | Public JPG, JPEG, or PNG URL for the landing page hero image. |
| `layout` | body | `string` | no | Landing page layout, CLASSIC or MODERN. |

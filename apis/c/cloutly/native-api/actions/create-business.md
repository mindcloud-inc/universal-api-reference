# Create Business with Cloutly

Creates a new business in Cloutly.

## Endpoint

- **Method:** `POST`
- **Path:** `https://marketplace.cloutly.com/api/v2/businesses`
- **Base URL:** `https://app.cloutly.com/api/v1`
- **API:** rest
- **Official documentation:** [Create Business](https://docs.cloutly.com/reviews-sdk-for-marketplace-websites/business-api/business-api-create-business)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Business name to create in Cloutly marketplace. |
| `senderName` | body | `string` | no | External-friendly display label for the business. |
| `address` | body | `string` | no | Business address. |
| `industry` | body | `string` | no | Business industry. |
| `website` | body | `string` | no | Business website URL or hostname. |
| `logoUrl` | body | `string` | no | Hosted logo URL for the business. |
| `googlePlaceId` | body | `string` | no | Google Place ID to connect Google review sources. |
| `facebookUrl` | body | `string` | no | Facebook page URL to connect Facebook review sources. |

# List Reviews with Cloutly

Retrieves reviews for connected sources in Cloutly.

## Endpoint

- **Method:** `GET`
- **Path:** `/reviews`
- **Base URL:** `https://app.cloutly.com/api/v1`
- **API:** rest
- **Official documentation:** [List Reviews](https://docs.cloutly.com/reviews-sdk-for-marketplace-websites/rest-api/list-reviews)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `businessId` | query | `string` | no | Filter reviews to one business. |
| `source` | query | `string` | no | Filter reviews by source. Accepted values: `0`, `1`. |
| `showOnWidget` | query | `boolean` | no | Filter by widget visibility. |

# List Reviews By Product with WiserReview

Retrieves reviews for a product from WiserReview.

## Endpoint

- **Method:** `GET`
- **Path:** `/reviewsByProduct`
- **Base URL:** `https://api.wiserreview.com/api/v1`
- **Official documentation:** [List Reviews By Product](https://apidocs.wiserreview.com/get-reviews-by-product-26190894e0)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `productId` | query | `string` | yes | Unique identifier of the product to fetch related reviews for. |

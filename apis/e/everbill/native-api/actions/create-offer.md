# Create Offer with Everbill

Creates a new offer in Everbill.

## Endpoint

- **Method:** `POST`
- **Path:** `/offers/add`
- **Base URL:** `https://api.everbill.eu`
- **Official documentation:** [Create Offer](https://api.swaggerhub.com/apis/everbill1/everbill/1.10/swagger.json#/paths/~1offers~1add/post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Offer` | body | `object` | yes | Offer object for the request body. |
| `Customer` | body | `object` | yes | Customer object for the request body. |
| `Address` | body | `object` | no | Address object for the request body. |
| `Article[]` | body | `array<object>` | no | Article array for the request body. |
| `Transaction[]` | body | `array<object>` | no | Transaction array for the request body. |

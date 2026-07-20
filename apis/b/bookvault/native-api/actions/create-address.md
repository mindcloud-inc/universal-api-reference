# Create Address with Bookvault

Creates a new address in Bookvault.

## Endpoint

- **Method:** `POST`
- **Path:** `/Addresses`
- **Base URL:** `https://api.bookvault.app/v3`
- **Official documentation:** [Create Address](https://api.bookvault.app/v3/docs#tag/Orders/operation/Addresses_post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `addr` | body | `object` | yes | Address payload to create in Bookvault. Required fields include Addressee, Address1, Town, and County. |

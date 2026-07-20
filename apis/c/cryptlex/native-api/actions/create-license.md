# Create License with Cryptlex

Creates a license in Cryptlex.

## Endpoint

- **Method:** `POST`
- **Path:** `/v3/licenses`
- **Base URL:** `https://api.cryptlex.com`
- **Official documentation:** [Create License](https://api.cryptlex.com/v3/docs#tag/Licenses/operation/post/v3/licenses)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `productId` | body | `string` | yes | Product to attach to the license. |
| `userId` | body | `string` | no | User linked to the license. |

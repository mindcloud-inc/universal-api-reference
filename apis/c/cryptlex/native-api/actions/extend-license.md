# Extend License with Cryptlex

Extends a license in Cryptlex.

## Endpoint

- **Method:** `POST`
- **Path:** `/v3/licenses/:id/extend`
- **Base URL:** `https://api.cryptlex.com`
- **Official documentation:** [Extend License](https://api.cryptlex.com/v3/docs#tag/Licenses/operation/post/v3/licenses/%7Bid%7D/extend)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Unique identifier for the license. |
| `extensionLength` | body | `number` | yes | License extension duration in seconds. |

# List Subscriptions with BlueSnap

Retrieves subscriptions from BlueSnap.

## Endpoint

- **Method:** `GET`
- **Path:** `/recurring/subscriptions`
- **Base URL:** `https://sandbox.bluesnap.com/services/2`
- **Official documentation:** [List Subscriptions](https://developers.bluesnap.com/v8976-JSON/reference/retrieve-all-subscriptions)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `after` | query | `string` | no | Return subscriptions after this subscription ID. |
| `before` | query | `string` | no | Return subscriptions before this subscription ID. |
| `pagesize` | query | `string` | no | Number of results to return. |
| `status` | query | `string` | no | Filter by subscription status. |
| `planId` | query | `string` | no | Filter by plan ID. |
| `vaultedShopperId` | query | `string` | no | Filter by vaulted shopper ID. |
| `gettotal` | query | `boolean` | no | Whether to include total results count. |
| `fulldescription` | query | `boolean` | no | Return full subscription details. |

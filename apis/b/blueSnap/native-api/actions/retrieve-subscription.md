# Retrieve Subscription with BlueSnap

Retrieves a subscription from BlueSnap.

## Endpoint

- **Method:** `GET`
- **Path:** `/recurring/subscriptions/:subscriptionId`
- **Base URL:** `https://sandbox.bluesnap.com/services/2`
- **Official documentation:** [Retrieve Subscription](https://developers.bluesnap.com/v8976-JSON/reference/retrieve-specific-subscription)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `subscriptionId` | path | `string` | yes | Subscription ID. |

# Get Subscription with Raisely

Retrieves a subscription from Raisely.

## Endpoint

- **Method:** `GET`
- **Path:** `/subscriptions/:uuid`
- **Base URL:** `https://api.raisely.com/v3`
- **Official documentation:** [Get Subscription](https://developers.raisely.com/reference/getsubscription)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `uuid` | path | `string` | yes | The `uuid` of the record |
| `private` | query | `boolean` | no | Returns the full record when authenticated |

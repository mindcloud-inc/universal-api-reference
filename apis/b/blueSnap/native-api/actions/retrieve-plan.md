# Retrieve Plan with BlueSnap

Retrieves a plan from BlueSnap.

## Endpoint

- **Method:** `GET`
- **Path:** `/recurring/plans/:planId`
- **Base URL:** `https://sandbox.bluesnap.com/services/2`
- **Official documentation:** [Retrieve Plan](https://developers.bluesnap.com/v8976-JSON/reference/retrieve-specific-plan)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `planId` | path | `string` | yes | Billing plan ID. |

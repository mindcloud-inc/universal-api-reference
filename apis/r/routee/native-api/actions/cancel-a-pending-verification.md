# Cancel a pending verification with Routee

Cancels a pending verification in Routee.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/2step/:trackingId`
- **Base URL:** `https://connect.routee.net`
- **Official documentation:** [Cancel a pending verification](https://docs.routee.net/reference/cancel-verification)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `trackingId` | path | `string` | yes | the tracking id of the verification. |

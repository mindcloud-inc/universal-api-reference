# Update Plan with BlueSnap

Updates a plan in BlueSnap.

## Endpoint

- **Method:** `PUT`
- **Path:** `/recurring/plans/:planId`
- **Base URL:** `https://sandbox.bluesnap.com/services/2`
- **Official documentation:** [Update Plan](https://developers.bluesnap.com/v8976-JSON/reference/update-plan)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `planId` | path | `string` | yes | Billing plan ID. |
| `status` | body | `string` | no | Plan status for updates (ACTIVE or INACTIVE). |

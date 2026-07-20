# Cancel Leave Request with Zoho People

Cancels a leave request in Zoho People.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/v3/leave-tracker/leaves/:recordId`
- **Base URL:** `https://people.zoho.com`
- **Official documentation:** [Cancel Leave Request](https://www.zoho.com/people/api/v3/leave-tracker/cancel-leave.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `recordId` | path | `string` | yes | Leave request record ID to cancel. |
| `reason` | body | `string` | no | Optional reason for cancelling the leave request. |

# Delete Leave Request with Zoho People

Deletes a leave request from Zoho People.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api/v3/leave-tracker/leaves/:recordId`
- **Base URL:** `https://people.zoho.com`
- **Official documentation:** [Delete Leave Request](https://www.zoho.com/people/api/v3/leave-tracker/delete-leave.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `recordId` | path | `string` | yes | Leave request record ID to delete. |

# This Endpoint Fetches The Requested Approvers Of A Change Request with Unleash

Retrieves change request approvers from Unleash.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/admin/projects/{projectId}/change-requests/{id}/approvers`
- **Base URL:** `https://us.app.getunleash.io/uspp0456`
- **Official documentation:** [This Endpoint Fetches The Requested Approvers Of A Change Request](https://docs.getunleash.io/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | Required path parameter. |
| `id` | path | `string` | yes | Required path parameter. |

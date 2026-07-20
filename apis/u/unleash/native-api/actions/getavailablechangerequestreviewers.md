# This Endpoint Will Return Users Available To Review/Approve This Change Request with Unleash

Retrieves available change request reviewers from Unleash.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/admin/projects/{projectId}/change-requests/available-reviewers/{environment}`
- **Base URL:** `https://us.app.getunleash.io/uspp0456`
- **Official documentation:** [This Endpoint Will Return Users Available To Review/Approve This Change Request](https://docs.getunleash.io/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | Required path parameter. |
| `environment` | path | `string` | yes | Required path parameter. |

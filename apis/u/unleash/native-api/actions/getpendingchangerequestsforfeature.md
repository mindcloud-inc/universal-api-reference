# Retrieves All Pending Change Requests Referencing A Feature In The Project with Unleash

Retrieves all pending change requests referencing a feature in the project from Unleash.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/admin/projects/{projectId}/change-requests/pending/{featureName}`
- **Base URL:** `https://us.app.getunleash.io/uspp0456`
- **Official documentation:** [Retrieves All Pending Change Requests Referencing A Feature In The Project](https://docs.getunleash.io/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | Required path parameter. |
| `featureName` | path | `string` | yes | Required path parameter. |

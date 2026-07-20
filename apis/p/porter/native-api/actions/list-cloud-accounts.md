# List Cloud Accounts with Porter

Retrieves cloud accounts from a Porter project.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/projects/:projectId/clouds`
- **Base URL:** `https://dashboard.porter.run`
- **Official documentation:** [List Cloud Accounts](https://docs.porter.run/cloud-accounts/overview)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | The Porter project ID whose connected cloud accounts you want to list. |

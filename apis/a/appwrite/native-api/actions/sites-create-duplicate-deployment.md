# Create duplicate deployment with Appwrite

Creates a new duplicate deployment in your Appwrite project.

## Endpoint

- **Method:** `POST`
- **Path:** `/sites/{siteId}/deployments/duplicate`
- **Base URL:** `https://cloud.appwrite.io/v1`
- **Official documentation:** [Create duplicate deployment](https://appwrite.io/docs/references/cloud/server-rest/sites)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `siteId` | path | `string` | yes | Site ID. |
| `deploymentId` | body | `string` | yes | Deployment ID. |

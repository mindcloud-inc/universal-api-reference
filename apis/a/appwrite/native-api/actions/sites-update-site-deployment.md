# Update site's deployment with Appwrite

Updates a site deployment in your Appwrite project.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/sites/{siteId}/deployment`
- **Base URL:** `https://cloud.appwrite.io/v1`
- **Official documentation:** [Update site's deployment](https://appwrite.io/docs/references/cloud/server-rest/sites)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `siteId` | path | `string` | yes | Site ID. |
| `deploymentId` | body | `string` | yes | Deployment ID. |

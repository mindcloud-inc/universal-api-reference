# Create template deployment with Appwrite

Creates a new template deployment in your Appwrite project.

## Endpoint

- **Method:** `POST`
- **Path:** `/sites/{siteId}/deployments/template`
- **Base URL:** `https://cloud.appwrite.io/v1`
- **Official documentation:** [Create template deployment](https://appwrite.io/docs/references/cloud/server-rest/sites)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `siteId` | path | `string` | yes | Site ID. |
| `repository` | body | `string` | yes | Repository name of the template. |
| `owner` | body | `string` | yes | The name of the owner of the template. |
| `rootDirectory` | body | `string` | yes | Path to site code in the template repo. |
| `type` | body | `string` | yes | Type for the reference provided. Can be commit, branch, or tag |
| `reference` | body | `string` | yes | Reference value, can be a commit hash, branch name, or release tag |
| `activate` | body | `boolean` | no | Automatically activate the deployment when it is finished building. |

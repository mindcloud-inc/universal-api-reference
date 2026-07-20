# Create VCS deployment with Appwrite

Creates a new VCS deployment in your Appwrite project.

## Endpoint

- **Method:** `POST`
- **Path:** `/functions/{functionId}/deployments/vcs`
- **Base URL:** `https://cloud.appwrite.io/v1`
- **Official documentation:** [Create VCS deployment](https://appwrite.io/docs/references/cloud/server-rest/functions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `functionId` | path | `string` | yes | Function ID. |
| `type` | body | `string` | yes | Type of reference passed. Allowed values are: branch, commit |
| `reference` | body | `string` | yes | VCS reference to create deployment from. Depending on type this can be: branch name, commit hash |
| `activate` | body | `boolean` | no | Automatically activate the deployment when it is finished building. |

# Create deployment with Appwrite

Creates a new deployment in your Appwrite project.

## Endpoint

- **Method:** `POST`
- **Path:** `/sites/{siteId}/deployments`
- **Base URL:** `https://cloud.appwrite.io/v1`
- **Official documentation:** [Create deployment](https://appwrite.io/docs/references/cloud/server-rest/sites)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `siteId` | path | `string` | yes | Site ID. |
| `installCommand` | body | `string` | no | Install Commands. |
| `buildCommand` | body | `string` | no | Build Commands. |
| `outputDirectory` | body | `string` | no | Output Directory. |
| `code` | body | `file` | yes | Gzip file with your code package. When used with the Appwrite CLI, pass the path to your code directory, and the CLI will automatically package your code. Use a path that is within the current directory. |
| `activate` | body | `boolean` | yes | Automatically activate the deployment when it is finished building. |

# Update variable with Appwrite

Updates the variable in your Appwrite project.

## Endpoint

- **Method:** `PUT`
- **Path:** `/functions/{functionId}/variables/{variableId}`
- **Base URL:** `https://cloud.appwrite.io/v1`
- **Official documentation:** [Update variable](https://appwrite.io/docs/references/cloud/server-rest/functions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `functionId` | path | `string` | yes | Function unique ID. |
| `variableId` | path | `string` | yes | Variable unique ID. |
| `key` | body | `string` | yes | Variable key. Max length: 255 chars. |
| `value` | body | `string` | no | Variable value. Max length: 8192 chars. |
| `secret` | body | `boolean` | no | Secret variables can be updated or deleted, but only functions can read them during build and runtime. |

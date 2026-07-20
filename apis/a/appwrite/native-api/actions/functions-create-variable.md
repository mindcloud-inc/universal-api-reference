# Create variable with Appwrite

Creates a new variable in your Appwrite project.

## Endpoint

- **Method:** `POST`
- **Path:** `/functions/{functionId}/variables`
- **Base URL:** `https://cloud.appwrite.io/v1`
- **Official documentation:** [Create variable](https://appwrite.io/docs/references/cloud/server-rest/functions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `functionId` | path | `string` | yes | Function unique ID. |
| `key` | body | `string` | yes | Variable key. Max length: 255 chars. |
| `value` | body | `string` | yes | Variable value. Max length: 8192 chars. |
| `secret` | body | `boolean` | no | Secret variables can be updated or deleted, but only functions can read them during build and runtime. |

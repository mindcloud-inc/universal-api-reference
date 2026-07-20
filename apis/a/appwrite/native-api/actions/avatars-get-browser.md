# Get browser icon with Appwrite

Retrieves a browser icon from Appwrite.

## Endpoint

- **Method:** `GET`
- **Path:** `/avatars/browsers/{code}`
- **Base URL:** `https://cloud.appwrite.io/v1`
- **Official documentation:** [Get browser icon](https://appwrite.io/docs/references/cloud/server-rest/avatars)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `code` | path | `file` | yes | Browser Code. |
| `width` | query | `number` | no | Image width. Pass an integer between 0 to 2000. Defaults to 100. |
| `height` | query | `number` | no | Image height. Pass an integer between 0 to 2000. Defaults to 100. |
| `quality` | query | `number` | no | Image quality. Pass an integer between 0 to 100. Defaults to keep existing image quality. |

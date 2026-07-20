# Upload File with Fibery

Creates a new file in Fibery.

## Endpoint

- **Method:** `POST`
- **Path:** `/files`
- **Base URL:** `https://{account}.fibery.io/api`
- **Official documentation:** [Upload File](https://the.fibery.io/@public/User_Guide/Guide/File-API-265)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `file` | body | `file` | yes |

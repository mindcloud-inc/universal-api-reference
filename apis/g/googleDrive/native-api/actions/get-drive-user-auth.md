# Get Drive User (Auth) with Google Drive

Gets information about the authenticated user, the user's Drive, and system capabilities.

## Endpoint

- **Method:** `GET`
- **Path:** `/drive/v3/about`
- **Base URL:** `https://www.googleapis.com`
- **Official documentation:** [Get Drive User (Auth)](https://developers.google.com/workspace/drive/api/reference/rest/v3/about/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fields` | query | `string` | no | Specify the fields to return for this method. (kind,user,storageQuota) Send multiple values as a array. |

# Update App Version with Clappia

Updates an existing app version in Clappia.

## Endpoint

- **Method:** `POST`
- **Path:** `/appdefinitionv2/updateAppVersion`
- **Base URL:** `https://api-public-v4.clappia.com`
- **Official documentation:** [Update App Version](https://developer.clappia.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `appId` | body | `string` | yes | Clappia app ID. |
| `initialVersionName` | body | `string` | yes | Current version name to rename. |
| `newVersionName` | body | `string` | yes | New name for the app version. |

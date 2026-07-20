# Create App Version with Clappia

Creates a new app version in Clappia.

## Endpoint

- **Method:** `POST`
- **Path:** `/appdefinitionv2/createNewAppVersion`
- **Base URL:** `https://api-public-v4.clappia.com`
- **Official documentation:** [Create App Version](https://developer.clappia.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `appId` | body | `string` | yes | Clappia app ID. |
| `versionName` | body | `string` | yes | Name for the new app version. |

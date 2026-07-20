# Update App Live Version with Clappia

Updates the live app version in Clappia.

## Endpoint

- **Method:** `POST`
- **Path:** `/appdefinitionv2/updateLiveVersion`
- **Base URL:** `https://api-public-v4.clappia.com`
- **Official documentation:** [Update App Live Version](https://developer.clappia.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `appId` | body | `string` | yes | Clappia app ID. |
| `versionVariableName` | body | `string` | yes | Variable name of the app version to make live. |

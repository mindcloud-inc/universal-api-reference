# Get Build Remote Access with Codemagic

Retrieves remote access details for a Codemagic build.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v3/builds/:build_id/remote-access`
- **Base URL:** `https://codemagic.io`
- **Official documentation:** [Get Build Remote Access](https://codemagic.io/api/v3/schema#tag/Builds/operation/ApiV3BuildsBuildIdRemoteAccessGetBuildRemoteAccess)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `build_id` | path | `string` | yes | Codemagic build identifier. |

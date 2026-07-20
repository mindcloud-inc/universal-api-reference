# Get Build with Codemagic

Retrieves a specific build from Codemagic.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v3/builds/:build_id`
- **Base URL:** `https://codemagic.io`
- **Official documentation:** [Get Build](https://codemagic.io/api/v3/schema#tag/Builds/operation/ApiV3BuildsBuildIdGetBuild)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `build_id` | path | `string` | yes | Codemagic build identifier. |

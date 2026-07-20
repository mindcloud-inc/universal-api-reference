# Get Build Actions with Codemagic

Retrieves actions for a specific Codemagic build.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v3/builds/:build_id/actions`
- **Base URL:** `https://codemagic.io`
- **Official documentation:** [Get Build Actions](https://codemagic.io/api/v3/schema#tag/Builds/operation/ApiV3BuildsBuildIdActionsGetBuildActions)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `build_id` | path | `string` | yes | Codemagic build identifier. |

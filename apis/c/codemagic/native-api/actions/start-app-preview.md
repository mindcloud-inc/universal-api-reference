# Start App Preview with Codemagic

Creates a new app preview for a Codemagic build.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v3/builds/:build_id/preview`
- **Base URL:** `https://codemagic.io`
- **Official documentation:** [Start App Preview](https://codemagic.io/api/v3/schema#tag/App%20Previews/operation/ApiV3BuildsBuildIdPreviewStartPreview)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `build_id` | path | `string` | yes | Codemagic build identifier. |
| `artifact_path` | body | `string` | yes | Path of the build artifact to preview. |

# Create Video From Template with Colossyan

Creates a video generation job from a Colossyan template.

## Endpoint

- **Method:** `POST`
- **Path:** `/video-generation-jobs/template-jobs`
- **Base URL:** `https://app.colossyan.com/api/v1`
- **Official documentation:** [Create Video From Template](https://docs.colossyan.com/video-generation/video-generation/generating-using-a-template)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `templateJobId` | body | `string` | yes | ID of the Colossyan template job to execute. |
| `dynamicVariables` | body | `object` | yes | Object of template variables to inject into the template. |
| `callbackUrl` | body | `string` | no | Optional callback URL for job completion events. |
| `callbackPayload` | body | `object` | no | Optional callback payload object. |

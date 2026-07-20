# Create Video Template with Bannerbear

Creates a new video template in Bannerbear.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/video_templates`
- **Base URL:** `https://api.bannerbear.com`
- **Official documentation:** [Create Video Template](https://developers.bannerbear.com/v2/#create-a-video-template)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `template` | body | `string` | yes | The existing image template UID to convert into a video template. |
| `render_type` | body | `string` | yes | The Bannerbear video build pack to use: overlay, transcribe, or multi_overlay. |
| `approval_required` | body | `boolean` | no | Whether manual approval is required before rendering videos from this template. |
| `transcription_layer_name` | body | `string` | no | The text layer name used for transcription output when render_type is transcribe. |

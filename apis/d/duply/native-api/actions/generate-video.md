# Generate Video with Duply

Creates a generated video from a Duply template.

## Endpoint

- **Method:** `POST`
- **Path:** `/generate-video/`
- **Base URL:** `https://gen.duply.co/v1`
- **Official documentation:** [Generate Video](https://app.duply.co/docs#post-generate-video)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `templateId` | body | `string` | yes | The ID of the template to generate from. |
| `formats[]` | body | `array<string>` | yes | Video output formats to generate. Duply currently documents mp4. |
| `fill` | body | `object` | yes | Template element values keyed by the element name. |
| `requestName` | body | `string` | no | Optional identifier for the generation request. |

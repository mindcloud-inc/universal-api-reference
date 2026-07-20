# Generate Image with Duply

Creates a generated image from a Duply template.

## Endpoint

- **Method:** `POST`
- **Path:** `/generate/`
- **Base URL:** `https://gen.duply.co/v1`
- **Official documentation:** [Generate Image](https://app.duply.co/docs#post-generate-image)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `templateId` | body | `string` | yes | The ID of the template to generate from. |
| `formats[]` | body | `array<string>` | yes | Image output formats to generate, such as jpg, png, or thumb. |
| `fill` | body | `object` | yes | Template element values keyed by the element name. |
| `requestName` | body | `string` | no | Optional identifier for the generation request. |
| `transparent` | body | `string` | no | Optional transparency flag used when generating png output. |
| `variantName` | body | `string` | no | Optional template variant name. Defaults to the oldest variant when omitted. |

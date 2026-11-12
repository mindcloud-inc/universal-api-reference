# Create Image with Google Slides

Inserts an image from a public URL onto a slide.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/presentations/[:presentationId]\:batchUpdate`
- **Base URL:** `https://slides.googleapis.com`
- **API:** rest
- **Official documentation:** [Create Image](https://developers.google.com/workspace/slides/api/reference/rest/v1/presentations/request#CreateImageRequest)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `presentationId` | path | `list<string>` | yes | The ID of the presentation to update. |
| `requests[0].createImage.url` | body | `string` | yes | Public PNG, JPEG or GIF URL, at most 2 KB long. The image must be under 50 MB and 25 megapixels. |
| `requests[0].createImage.elementProperties` | body | `object` | no | — |
| `elementProperties.pageObjectId` | body | `string` | yes | The object ID of the slide the element is placed on. |
| `elementProperties.size` | body | `object` | no | — |
| `elementProperties.size.width` | body | `object` | no | — |
| `elementProperties.size.width.magnitude` | body | `number` | no | — |
| `elementProperties.size.width.unit` | body | `list<string>` | no | Accepted values: `EMU`, `PT`, `UNIT_UNSPECIFIED`. |
| `elementProperties.size.height` | body | `object` | no | — |
| `elementProperties.size.height.magnitude` | body | `number` | no | — |
| `elementProperties.size.height.unit` | body | `list<string>` | no | Accepted values: `EMU`, `PT`, `UNIT_UNSPECIFIED`. |
| `elementProperties.transform` | body | `object` | no | — |
| `elementProperties.transform.scaleX` | body | `number` | no | — |
| `elementProperties.transform.scaleY` | body | `number` | no | — |
| `elementProperties.transform.shearX` | body | `number` | no | — |
| `elementProperties.transform.shearY` | body | `number` | no | — |
| `elementProperties.transform.translateX` | body | `number` | no | — |
| `elementProperties.transform.translateY` | body | `number` | no | — |
| `elementProperties.transform.unit` | body | `list<string>` | no | Units for the translate elements. Accepted values: `EMU`, `PT`, `UNIT_UNSPECIFIED`. |
| `requests[0].createImage.objectId` | body | `string` | no | Optional custom ID for the new object: 5-50 characters, starting with a letter, digit or underscore. Generated when omitted. |

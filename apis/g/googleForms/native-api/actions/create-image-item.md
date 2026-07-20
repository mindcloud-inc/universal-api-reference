# Create Image Item with Google Forms

Creates an image item in Google Forms.

## Endpoint

- **Method:** `POST`
- **Path:** `/:formId:batchUpdate`
- **Base URL:** `https://forms.googleapis.com/v1/forms`
- **Official documentation:** [Create Image Item](https://developers.google.com/workspace/forms/api/reference/rest/v1/forms/batchUpdate)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `formId` | path | `string` | yes | The form identifier. |
| `title` | body | `string` | no | Optional item title. |
| `sourceUri` | body | `string` | yes | Source URI for the image. |
| `altText` | body | `string` | no | Alternative text for accessibility. |
| `alignment` | body | `list` | no | How to align the image in the form. Accepted values: `0`, `1`, `2`. |
| `width` | body | `number` | no | Image width in pixels. |
| `locationIndex` | body | `number` | yes | Where to place the new image item in the form. |

# Get Template Preview with Print.one Postcards

Retrieves a template preview from Print.one Postcards.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/storage/template/preview/[:previewId]`
- **Base URL:** `https://api.print.one`
- **Official documentation:** [Get Template Preview](https://api.print.one/docs/v2#operation/Storage/getTemplatePreview)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `previewId` | path | `string` | yes | The ID of the preview |
| `asPdf` | query | `boolean` | yes | Whether to return the preview as a PDF |

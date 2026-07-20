# Get Template Preview Details with Print.one Postcards

Retrieves template preview details from Print.one Postcards.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/storage/template/preview/[:previewId]/details`
- **Base URL:** `https://api.print.one`
- **Official documentation:** [Get Template Preview Details](https://api.print.one/docs/v2#operation/Storage/getTemplatePreviewDetails)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `previewId` | path | `string` | yes | The ID of the preview |
| `asPdf` | query | `boolean` | yes | Whether the preview was rendered as a PDF |

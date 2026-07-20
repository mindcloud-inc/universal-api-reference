# Get Extraction Data with Typless

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/get-extraction-data`
- **Base URL:** `https://developers.typless.com`
- **Official documentation:** [Get Extraction Data](https://typless.gitbook.io/typlessapi/typless/data-extraction/asynchronous-extraction)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `extraction_id` | query | `string` | yes | Typless extraction job identifier. |
| `text_blocks` | query | `boolean` | no | Whether to include text block details in the extraction response. |

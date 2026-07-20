# Extract Pretrained Model Data with Typless

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/pretrained-models/[:model_name]`
- **Base URL:** `https://developers.typless.com`
- **Official documentation:** [Extract Pretrained Model Data](https://typless.gitbook.io/typlessapi/methods/extract-data-with-pretrained-model)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `model_name` | path | `string` | yes | Pretrained Typless model to use for extraction. Accepted values: `0`, `1`, `2`, `3`, `4`, `5`, `6`, `7`. |
| `file_name` | body | `string` | yes | Original filename of the document being processed by the pretrained model. |
| `file` | body | `string` | no | Base64-encoded file content for pretrained-model extraction. |
| `file_url` | body | `string` | no | Public URL to the file for pretrained-model extraction. |
| `for_customer` | body | `string` | no | Optional customer identifier for pretrained-model extraction. |

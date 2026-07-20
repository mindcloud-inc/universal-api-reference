# Create Text Analysis with Humantic AI

## Endpoint

- **Method:** `POST`
- **Path:** `/user-profile/create`
- **Base URL:** `https://api.humantic.ai/v1`
- **Official documentation:** [Create Text Analysis](https://api.humantic.ai/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | query | `string` | yes | Unique identifier for the text analysis. Do not use values starting with `test`. |
| `text` | body | `string` | yes | Free-form text to analyze. Humantic recommends at least 300 words and processes only the first 10,000 words. |
| `stateless` | query | `boolean` | no | When true, Humantic does not save text input data. Applies only to text or document input. |
| `analysistype` | query | `string` | no | Use `talent` for English text or document input intended for hiring or talent assessment. |

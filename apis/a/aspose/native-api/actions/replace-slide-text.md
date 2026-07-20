# Replace Slide Text with Aspose

Replaces text within a slide in Aspose.

## Endpoint

- **Method:** `POST`
- **Path:** `/slides/:name/slides/:slideIndex/replaceText`
- **Base URL:** `https://api.aspose.cloud/v3.0`
- **Official documentation:** [Replace Slide Text](https://docs.aspose.cloud/slides/replace-a-text-occurrence/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | path | `string` | yes | The presentation file name. |
| `slideIndex` | path | `number` | yes | The 1-based slide index. |
| `oldValue` | query | `string` | yes | The text value to replace. |
| `newValue` | query | `string` | yes | The replacement text value. |

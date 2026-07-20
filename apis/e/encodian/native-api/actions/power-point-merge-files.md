# PowerPoint Merge Files with Encodian

Merges PowerPoint files in Encodian.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/PowerPoint/MergePresentations`
- **Base URL:** `https://api.apps-encodian.com`
- **Official documentation:** [PowerPoint Merge Files](https://support.encodian.com/hc/en-gb/articles/4425652063761)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `mergePresentationOutputFormat` | body | `string` | yes | The output presentation format, such as PPTX. |
| `outputFilename` | body | `string` | no | Optional filename for the merged presentation; defaults to presentation. |
| `documents[]` | body | `array<object>` | yes | Array of presentations to merge. Each item includes fileName, fileContent, optional sortPosition, and optional slidesToMerge. |
| `mergePresentationMasterStyle` | body | `boolean` | no | Apply the first presentation style to all other presentations. |

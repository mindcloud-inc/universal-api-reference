# Utilities - Concatenate Text with Encodian - Utilities

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/Utilities/ConcatenateText`
- **Base URL:** `https://api.apps-encodian.com`
- **Official documentation:** [Utilities - Concatenate Text](https://support.encodian.com/hc/en-gb/articles/11873576674077)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `textList[]` | body | `array<string>` | no | The array of text values to concatenate |
| `delimiter` | body | `string` | no | The delimiter to place between the concatenated text values |
| `trimResult` | body | `boolean` | no | Set whether white-space should be trimmed from the processed text value |

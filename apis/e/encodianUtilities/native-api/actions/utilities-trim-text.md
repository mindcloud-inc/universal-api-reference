# Utilities - Trim Text with Encodian - Utilities

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/Utilities/TrimText`
- **Base URL:** `https://api.apps-encodian.com`
- **Official documentation:** [Utilities - Trim Text](https://support.encodian.com/hc/en-gb/articles/11769860640413)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `text` | body | `string` | yes | The text value to process |
| `textTrimPosition` | body | `string` | yes | Set whether to trim the text provided from the start position, end position or both Accepted values: `0`, `1`, `2`. |
| `trimCharacters` | body | `string` | no | Optional - A list of characters (which can include white-space) to trim from the text provided, for example: &*yt^ :{ |

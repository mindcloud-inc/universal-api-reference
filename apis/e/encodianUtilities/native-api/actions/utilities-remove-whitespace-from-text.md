# Utilities - Remove Whitespace from Text with Encodian - Utilities

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/Utilities/RemoveWhitespaceFromText`
- **Base URL:** `https://api.apps-encodian.com`
- **Official documentation:** [Utilities - Remove Whitespace from Text](https://support.encodian.com/hc/en-gb/articles/23853140876316)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `text` | body | `string` | yes | The text value to process |
| `removalType` | body | `string` | no | Set the types of whitespace which should be removed from the 'Text' value provided Accepted values: `0`, `1`, `2`. |

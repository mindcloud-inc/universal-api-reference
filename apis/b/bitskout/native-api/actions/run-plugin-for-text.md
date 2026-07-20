# Run Plugin for Text with Bitskout

Runs a Bitskout plugin on text.

## Endpoint

- **Method:** `POST`
- **Path:** `/powerauto/run_text`
- **Base URL:** `https://api.bitskout.com/v2`
- **Official documentation:** [Run Plugin for Text](https://learn.microsoft.com/en-us/connectors/bitskout/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `plugin` | body | `list<string>` | yes | Unique Plugin ID returned by List Plugins. |
| `text` | body | `string` | yes | Text to analyze with the selected Bitskout plugin. |

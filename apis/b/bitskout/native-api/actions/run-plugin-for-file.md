# Run Plugin for File with Bitskout

Runs a Bitskout plugin on a file.

## Endpoint

- **Method:** `POST`
- **Path:** `/powerauto/run_file`
- **Base URL:** `https://api.bitskout.com/v2`
- **Official documentation:** [Run Plugin for File](https://learn.microsoft.com/en-us/connectors/bitskout/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `plugin` | body | `list<string>` | yes | Unique Plugin ID returned by List Plugins. |
| `file_url` | body | `string` | yes | Direct download URL for the file that Bitskout should process. |

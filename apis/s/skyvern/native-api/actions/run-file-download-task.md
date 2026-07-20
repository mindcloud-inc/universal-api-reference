# Run File Download Task with Skyvern

Runs a file download task in Skyvern.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/run/tasks/download_files`
- **Base URL:** `https://api.skyvern.com`
- **Official documentation:** [Run File Download Task](https://www.skyvern.com/docs/api-reference/agent/file-download-task)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `navigation_goal` | body | `string` | yes | Instructions for navigating to and downloading the file. |
| `url` | body | `string` | no | Website URL for the download task. |

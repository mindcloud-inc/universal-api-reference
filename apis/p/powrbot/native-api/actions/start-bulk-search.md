# Start Bulk Search with Powrbot

Creates a bulk search job in Powrbot.

## Endpoint

- **Method:** `POST`
- **Path:** `/search/`
- **Base URL:** `https://powrbot.com/api/v1`
- **Official documentation:** [Start Bulk Search](https://powrbot.com/cpages/docs/)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `csv_file` | body | `file` | yes | CSV file containing company names, one per row. |

# List Folders with Google Drive

Lists all Google Drive Folders. Optionally search folders you have access to in a Team Drive.

## Endpoint

- **Method:** `GET`
- **Path:** `/drive/v3/files`
- **Base URL:** `https://www.googleapis.com`
- **Official documentation:** [List Folders](https://developers.google.com/workspace/drive/api/reference/rest/v3/files/list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `q` | query | `string` | no | Search for folders based on specific parameters. Uses `q` param. See more here: https://developers.google.com/drive/api/guides/search-files |
| `orderBy` | query | `list<string>` | no | Choose one or multiple order options to sort the results. |

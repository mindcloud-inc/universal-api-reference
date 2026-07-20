# Import Products Via CSV with Zakeke

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/csv/import`
- **Base URL:** `https://api.zakeke.com`
- **Official documentation:** [Import Products Via CSV](https://docs.zakeke.com/docs/API/Integration/Connecting-Product/CSV-method#2-first-step-upload-the-csv-zip-file)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file` | body | `file` | yes | ZIP archive containing the required CSV files for the import task. |

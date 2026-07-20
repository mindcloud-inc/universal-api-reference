# Create Import URL Task with CloudConvert

Creates an import-by-URL task in CloudConvert.

## Endpoint

- **Method:** `POST`
- **Path:** `/import/url`
- **Base URL:** `https://api.cloudconvert.com/v2`
- **Official documentation:** [Create Import URL Task](https://cloudconvert.com/docs/import-export/import-files)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | Source URL to import from. |
| `filename` | body | `string` | no | Optional filename to assign to the imported file. |
| `headers` | body | `object` | no | Optional HTTP headers to send when fetching the source URL. |

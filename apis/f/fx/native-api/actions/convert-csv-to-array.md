# Convert CSV to Array with 1001fx

Converts a CSV file into an array of objects.

## Endpoint

- **Method:** `POST`
- **Path:** `/files/csv2array`
- **Base URL:** `https://api.1001fx.com`
- **Official documentation:** [Convert CSV to Array](https://1001fx.com/functions/csv2array)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `dynamicTyping` | body | `boolean` | no |
| `file` | body | `file` | yes |
| `header` | body | `boolean` | no |

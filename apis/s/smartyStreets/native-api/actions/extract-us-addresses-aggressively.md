# Extract US Addresses Aggressively with Smarty-streets

Extracts US addresses from text in Smarty-streets using aggressive matching.

## Endpoint

- **Method:** `POST`
- **Path:** `https://us-extract.api.smarty.com/`
- **Base URL:** `https://us-street.api.smarty.com`
- **Official documentation:** [Extract US Addresses Aggressively](https://www.smarty.com/docs/apis/us-extract-api/reference)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `text/plain; charset=utf-8` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `text` | body | `string` | yes | Text containing addresses to extract. |

# Download Credit Note File with Lexware Office

Downloads a credit note file from Lexware Office.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/credit-notes/:id/file`
- **Base URL:** `https://api.lexware.io`
- **Official documentation:** [Download Credit Note File](https://developers.lexware.io/docs/#credit-notes-endpoint-download-a-credit-note-file)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `*/*` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The Lexware credit note ID. |

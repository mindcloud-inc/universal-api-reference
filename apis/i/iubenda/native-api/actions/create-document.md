# Create Document with iubenda

Creates a document in iubenda.

## Endpoint

- **Method:** `POST`
- **Path:** `/beta/documents`
- **Base URL:** `https://consent.iubenda.com`
- **Official documentation:** [Create Document](https://www.iubenda.com/en/help/6484-consent-solution-http-api-documentation/#document)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file` | body | `file` | yes | Document file to upload. Max 1MB. |

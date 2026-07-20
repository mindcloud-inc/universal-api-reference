# Create Document Type with Zoho Sign

Creates a document type in Zoho Sign.

## Endpoint

- **Method:** `POST`
- **Path:** `/requesttypes`
- **Base URL:** `https://sign.zoho.com/api/v1`
- **Official documentation:** [Create Document Type](https://www.zoho.com/sign/api/document-managment/create-new-document-type.html)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/x-www-form-urlencoded` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data` | body | `object` | yes | Zoho Sign document type payload wrapper. |
| `data.request_types` | body | `object` | yes | Document type details. |
| `data.request_types.request_type_name` | body | `string` | yes | Name of the document type to create. |
| `data.request_types.request_type_description` | body | `string` | no | Description of the document type. |

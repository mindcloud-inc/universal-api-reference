# Download FBM Report Document (Presigned URL) with Amazon Seller

Downloads an FBM report document from Amazon Seller.

## Endpoint

- **Method:** `GET`
- **URL:** `:downloadUrl`
- **API:** REST
- **Official documentation:** [Download FBM Report Document (Presigned URL)](https://developer-docs.amazon.com/sp-api/docs/reports-api-v2021-06-30-reference#getreportdocument)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json; charset=utf-8` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `downloadUrl` | path | `string` | yes |

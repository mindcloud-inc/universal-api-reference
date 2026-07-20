# Extend Document Expiry with Zoho Sign

Extends document expiry in Zoho Sign.

## Endpoint

- **Method:** `PUT`
- **Path:** `/requests/:requestId/extend`
- **Base URL:** `https://sign.zoho.com/api/v1`
- **Official documentation:** [Extend Document Expiry](https://www.zoho.com/sign/api/document-managment/extend-document.html)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/x-www-form-urlencoded` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `requestId` | path | `string` | yes | Zoho Sign request identifier. |
| `expire_by` | body | `string` | yes | New expiry date for the document, for example 30 November 2024. |

# List Customers Modified Since with IRIS KashFlow

## Endpoint

- **Method:** `POST`
- **Path:** `/api/service.asmx`
- **Base URL:** `https://securedwebapp.com`
- **Official documentation:** [List Customers Modified Since](https://www.kashflow.com/developers/soap-api/getcustomersmodifiedsince/)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `text/xml; charset=utf-8` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `ModifiedSince` | body | `date` | yes |

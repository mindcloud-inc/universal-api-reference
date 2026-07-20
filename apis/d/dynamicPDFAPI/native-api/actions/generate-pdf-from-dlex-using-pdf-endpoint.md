# Generate PDF From DLEX Using PDF Endpoint with DynamicPDF

Generates a PDF from DLEX using DynamicPDF API.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1.0/pdf`
- **Base URL:** `https://api.dpdf.io`
- **Official documentation:** [Generate PDF From DLEX Using PDF Endpoint](https://dpdf.io/docs/usersguide/cloud-api/client-libraries/pdf-endpoint/pdf-inputs)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Instructions` | body | `object` | yes | PDF endpoint instructions payload using a DLEX input and inline resources. |

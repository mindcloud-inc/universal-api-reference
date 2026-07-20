# Merge Mixed Resources Into PDF with DynamicPDF

Merges mixed resources into a PDF in DynamicPDF API.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1.0/pdf`
- **Base URL:** `https://api.dpdf.io`
- **Official documentation:** [Merge Mixed Resources Into PDF](https://dpdf.io/docs/tutorials/cloud-api/dlex-pdf-endpoint)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Instructions` | body | `object` | yes | PDF endpoint instructions payload with mixed inputs and inline resources. |

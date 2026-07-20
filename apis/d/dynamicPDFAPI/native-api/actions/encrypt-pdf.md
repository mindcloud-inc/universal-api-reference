# Encrypt PDF with DynamicPDF

Encrypts a PDF in DynamicPDF API.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1.0/pdf`
- **Base URL:** `https://api.dpdf.io`
- **Official documentation:** [Encrypt PDF](https://dpdf.io/docs/encrypt-pdfs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Instructions` | body | `object` | yes | DynamicPDF instructions document sent as raw JSON. |

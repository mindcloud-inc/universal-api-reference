# Add PDF Bookmarks with DynamicPDF

Adds bookmarks to a PDF in DynamicPDF API.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1.0/pdf`
- **Base URL:** `https://api.dpdf.io`
- **Official documentation:** [Add PDF Bookmarks](https://dpdf.io/docs/add-bookmarks-to-pdf)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Instructions` | body | `object` | yes | DynamicPDF instructions document sent as raw JSON. |

# Create PDF From JSON with DynamicPDF

Creates a PDF from JSON in DynamicPDF API.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1.0/pdf`
- **Base URL:** `https://api.dpdf.io`
- **Official documentation:** [Create PDF From JSON](https://dpdf.io/docs/usersguide/cloud-api/cloud-api-pdf-json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Instructions` | body | `object` | yes | DynamicPDF instructions document sent as raw JSON. |

# Set PDF Metadata with DynamicPDF

Sets PDF metadata in DynamicPDF API.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1.0/pdf`
- **Base URL:** `https://api.dpdf.io`
- **Official documentation:** [Set PDF Metadata](https://dpdf.io/docs/usersguide/cloud-api/schemas/cloud-api-schema-pdf)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Instructions` | body | `object` | yes | DynamicPDF instructions document sent as raw JSON. |

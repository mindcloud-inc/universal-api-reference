# Flatten PDF Form Fields with DynamicPDF

Flattens PDF form fields in DynamicPDF API.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1.0/pdf`
- **Base URL:** `https://api.dpdf.io`
- **Official documentation:** [Flatten PDF Form Fields](https://dpdf.io/docs/flatten-or-delete-pdf-form-fields)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Instructions` | body | `object` | yes | DynamicPDF instructions document sent as raw JSON. |

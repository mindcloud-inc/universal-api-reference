# Get PDF Form Fields Info with PDF.co

Retrieves PDF form field info from PDF.co.

## Endpoint

- **Method:** `POST`
- **Path:** `/pdf/info/fields`
- **Base URL:** `https://api.pdf.co/v1`
- **Official documentation:** [Get PDF Form Fields Info](https://docs.pdf.co/api-tester/forms/info-reader)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | Source PDF URL. |
| `password` | body | `string` | no | Password for protected PDF. |
| `async` | body | `boolean` | no | Set true to run as async job. |

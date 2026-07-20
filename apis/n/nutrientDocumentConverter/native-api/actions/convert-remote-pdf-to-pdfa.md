# Convert Remote PDF to PDF/A with Nutrient Document Converter

Converts a remote PDF to PDF/A in Nutrient.

## Endpoint

- **Method:** `POST`
- **Path:** `/build`
- **Base URL:** `https://api.nutrient.io`
- **Official documentation:** [Convert Remote PDF to PDF/A](https://www.nutrient.io/guides/dws-processor/tools-and-api/pdf-to-pdfa-api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `pdfUrl` | body | `string` | yes | Publicly reachable PDF URL. |
| `conformance` | body | `string` | no | PDF/A conformance level, for example pdfa-2b. |

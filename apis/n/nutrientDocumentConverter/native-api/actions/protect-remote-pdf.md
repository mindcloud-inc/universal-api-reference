# Protect Remote PDF with Nutrient Document Converter

Protects a remote PDF in Nutrient.

## Endpoint

- **Method:** `POST`
- **Path:** `/build`
- **Base URL:** `https://api.nutrient.io`
- **Official documentation:** [Protect Remote PDF](https://www.nutrient.io/guides/dws-processor/tools-and-api/pdf-security-api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `pdfUrl` | body | `string` | yes | Publicly reachable PDF URL. |
| `userPassword` | body | `string` | yes | Password required to open the output PDF. |
| `ownerPassword` | body | `string` | no | Owner password used to control permissions. |
| `allowPrinting` | body | `boolean` | no | Whether printing is allowed in the output PDF. |

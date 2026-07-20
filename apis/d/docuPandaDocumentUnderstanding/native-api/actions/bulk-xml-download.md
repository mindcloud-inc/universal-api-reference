# Bulk Download Standardization XMLs with DocuPanda - Document Understanding

Creates a bulk standardization XML download URL in DocuPanda.

## Endpoint

- **Method:** `POST`
- **Path:** `/standardization/download/bulk-xml`
- **Base URL:** `https://app.docupipe.ai`
- **Official documentation:** [Bulk Download Standardization XMLs](https://docs.docupipe.ai/reference/bulk_xml_download)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `standardizationIds` | body | `list<string>` | yes | List of standardization IDs to download as XML files. |
| `standardizationIds[]` | body | `array<string>` | yes | List of standardization IDs to download as XML files. |

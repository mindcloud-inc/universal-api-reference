# Embed Field Placement with Docubee

Creates an embedded field placement session in Docubee.

## Endpoint

- **Method:** `POST`
- **Path:** `/embed`
- **Base URL:** `https://docubee.app/api/v2`
- **Official documentation:** [Embed Field Placement](https://docs.docubee.app/#embedded-field-placement)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `documentId` | body | `string` | no | The document to configure with embedded field placement. |
| `domain` | body | `string` | no | The whitelisted host domain for the embedded page. |

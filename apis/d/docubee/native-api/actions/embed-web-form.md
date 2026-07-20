# Embed Web Form with Docubee

Creates an embedded web form session in Docubee.

## Endpoint

- **Method:** `POST`
- **Path:** `/embed`
- **Base URL:** `https://docubee.app/api/v2`
- **Official documentation:** [Embed Web Form](https://docs.docubee.app/#embedded-web-forms)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `domain` | body | `string` | no | The whitelisted host domain for the embedded page. |
| `formId` | body | `string` | no | The published Docubee form ID extracted from the form URL. |

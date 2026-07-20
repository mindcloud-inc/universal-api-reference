# Merge PDFs with Placid

Merges PDFs in Placid from source URLs.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/rest/pdfs/merge`
- **Base URL:** `https://api.placid.app`
- **Official documentation:** [Merge PDFs](https://placid.app/docs/2.0/rest/pdfs#merge)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `urls[]` | body | `array<string>` | yes |
| `webhook_success` | body | `string` | no |
| `passthrough` | body | `string` | no |
| `transfer` | body | `object` | no |

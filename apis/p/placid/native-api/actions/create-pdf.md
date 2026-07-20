# Create PDF with Placid

Creates a new PDF in Placid from template pages.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/rest/pdfs`
- **Base URL:** `https://api.placid.app`
- **Official documentation:** [Create PDF](https://placid.app/docs/2.0/rest/pdfs#create)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `webhook_success` | body | `string` | no |
| `passthrough` | body | `string` | no |
| `pages[]` | body | `array<object>` | no |
| `pages[].template_uuid` | body | `string` | no |
| `pages[].layers` | body | `object` | no |
| `transfer` | body | `object` | no |
| `modifications` | body | `object` | no |

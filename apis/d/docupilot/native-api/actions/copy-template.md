# Copy Template with Docupilot

Copies a template in Docupilot.

## Endpoint

- **Method:** `POST`
- **Path:** `/dashboard/api/v2/templates/{id}/copy/`
- **Base URL:** `https://api.docupilot.app`
- **Official documentation:** [Copy Template](https://help.docupilot.app/developers/templates-api)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
| `folder` | body | `number` | yes |
| `title` | body | `string` | yes |

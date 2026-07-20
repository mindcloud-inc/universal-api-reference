# Create Template with PostGrid Print & Mail

Creates a template in PostGrid Print & Mail.

## Endpoint

- **Method:** `POST`
- **Path:** `/templates`
- **Base URL:** `https://api.postgrid.com/print-mail/v1`
- **Official documentation:** [Create Template](https://postgrid.readme.io/reference/templates_create-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `html` | body | `string` | no | The HTML content for the template. |
| `description` | body | `string` | no | An optional description visible in the API and dashboard. |
| `metadata` | body | `object` | no | Custom metadata for this template. |

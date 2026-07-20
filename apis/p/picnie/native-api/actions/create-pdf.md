# Create PDF with Picnie

Creates a PDF in Picnie from a template.

## Endpoint

- **Method:** `POST`
- **Path:** `/create-pdf`
- **Base URL:** `https://picnie.com/api/v1`
- **Official documentation:** [Create PDF](https://documenter.getpostman.com/view/25712226/2s93CGRvy6)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | body | `number` | yes | Project ID that will own the generated PDF. |
| `template_id` | body | `number` | yes | Template ID to use for PDF generation. |
| `template_name` | body | `string` | yes | Template name expected by Picnie. |
| `details` | body | `object<object>` | yes | Template field values to merge into the generated PDF. |

# Create Webpage PDF With Webhook Object ID and Type with DocMaker

Creates a webpage PDF with webhook object details in DocMaker.

## Endpoint

- **Method:** `POST`
- **Path:** `/page_pdf`
- **Base URL:** `https://api.v2.docmaker.co`
- **Official documentation:** [Create Webpage PDF With Webhook Object ID and Type](https://guide.docmaker.co/features/print-web-page-to-pdf/page_pdf-api-parameters)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `name` | body | `string` | yes |
| `url` | body | `string` | yes |
| `pageSize` | body | `string` | yes |
| `landscape` | body | `boolean` | yes |
| `webhook_url` | body | `string` | yes |
| `webhook_object_id` | body | `string` | yes |
| `webhook_object_type` | body | `string` | yes |

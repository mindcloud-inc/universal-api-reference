# Search Space with DocuWriter.ai

## Endpoint

- **Method:** `POST`
- **Path:** `/api/spaces/{{space}}/search`
- **Base URL:** `https://app.docuwriter.ai`
- **Official documentation:** [Search Space](https://docs.docuwriter.ai/docuwriterai-api-docs/92055)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `highlight` | body | `boolean` | no | Whether to wrap matched terms in mark tags. |
| `page` | body | `number` | no | Page number for paginated results. |
| `per_page` | body | `number` | no | Number of results per page. |
| `query` | body | `string` | yes | Search keyword or phrase. |
| `space` | path | `string` | yes | Space ID or slug to search within. |

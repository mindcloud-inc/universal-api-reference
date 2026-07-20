# Bulk Import URLs with jo4.io

## Endpoint

- **Method:** `POST`
- **Path:** `/protected/url/bulk-import`
- **Base URL:** `https://jo4-api.jo4.io/api/v1`
- **Official documentation:** [Bulk Import URLs](https://jo4-api.jo4.io/swagger-ui/index.html#/url-controller/bulkImport)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `urls[]` | body | `array<object>` | yes |

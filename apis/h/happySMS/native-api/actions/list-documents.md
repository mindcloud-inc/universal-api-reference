# List Documents with Happy SMS

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/protected/domain/custom-data/documents`
- **Base URL:** `https://www.api.nc`
- **Official documentation:** [List Documents](https://www.happy.nc/docs/sms.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `page` | query | `number` | no | Zero-based page number. |
| `limit` | query | `number` | no | Maximum number of documents to return. |
| `sort` | query | `string` | no | Sort expression such as key;ASC. |
| `queryFilter` | query | `string` | no | RSQL filter expression for narrowing documents. |

# Search Messages with Happy SMS

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/protected/domain/sms/messages/lookup`
- **Base URL:** `https://www.api.nc`
- **Official documentation:** [Search Messages](https://www.happy.nc/docs/sms.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `page` | query | `number` | no | Zero-based page number. |
| `limit` | query | `number` | no | Maximum number of messages to return. |
| `sort` | query | `string` | no | Sort expression such as lastStatusDate;DESC. |
| `fullText` | query | `string` | yes | Required text to search across messages. |

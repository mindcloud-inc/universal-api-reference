# List Messages with Happy SMS

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/protected/domain/sms/messages`
- **Base URL:** `https://www.api.nc`
- **Official documentation:** [List Messages](https://www.happy.nc/docs/sms.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `page` | query | `number` | no | Zero-based page number. |
| `limit` | query | `number` | no | Maximum number of messages to return. |
| `sort` | query | `string` | no | Sort expression such as lastStatusDate;DESC. |
| `queryFilter` | query | `string` | no | RSQL filter expression for narrowing messages. |

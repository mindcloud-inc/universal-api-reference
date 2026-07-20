# List Messages with SendMe

## Endpoint

- **Method:** `GET`
- **Path:** `/api/messages`
- **Base URL:** `https://app.sendme123.com`
- **Official documentation:** [List Messages](https://docs.sendme123.com/en/api/messages/list/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `endDate` | query | `string` | no | End date (ISO 8601). |
| `limit` | query | `number` | no | Items per page (default 20, max 100). |
| `page` | query | `number` | no | Page number (default 1). |
| `search` | query | `string` | no | Search in message content. |
| `startDate` | query | `string` | no | Start date (ISO 8601). |
| `status` | query | `string` | no | Filter by message status. |
| `type` | query | `string` | no | Filter by message type (sms or email). |

# List Email Issues with Feathery

## Endpoint

- **Method:** `GET`
- **Path:** `/api/logs/email/issues/`
- **Base URL:** `https://api.feathery.io`
- **Official documentation:** [List Email Issues](https://api-docs.feathery.io/#list-email-issues)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `event_type` | query | `string` | no | Filter to `Bounce` or `Complaint` events. Accepted values: `0`, `1`. |
| `start_time` | query | `date` | no | Only return email events after this time. |
| `end_time` | query | `date` | no | Only return email events before this time. |

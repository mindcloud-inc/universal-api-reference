# Get Analytics By Date with MailerSend

## Endpoint

- **Method:** `GET`
- **Path:** `/analytics/date`
- **Base URL:** `https://api.mailersend.com/v1`
- **Official documentation:** [Get Analytics By Date](https://developers.mailersend.com/api/v1/analytics#activity-data-by-date)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `date_from` | query | `string` | yes | Start datetime for analytics results in YYYY-MM-DD HH:mm:ss format. |
| `date_to` | query | `string` | yes | End datetime for analytics results in YYYY-MM-DD HH:mm:ss format. |
| `event` | query | `string` | yes | Analytics event types to include. Send multiple values as a array. |

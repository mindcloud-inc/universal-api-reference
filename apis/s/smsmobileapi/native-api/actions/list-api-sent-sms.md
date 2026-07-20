# List API Sent SMS with Smsmobileapi

Retrieves SMS messages sent through Smsmobileapi.

## Endpoint

- **Method:** `GET`
- **Path:** `/log/sent/sms/`
- **Base URL:** `https://api.smsmobileapi.com`
- **Official documentation:** [List API Sent SMS](https://smsmobileapi.com/doc/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `guid_message` | query | `string` | no | Filter the log to one exact SMS GUID. |
| `keyword` | query | `string` | no | Filter by recipient number or message content. |
| `error_api` | query | `list` | no | Only return SMS entries that have an API request error. Accepted values: `1`. |
| `error_mobile` | query | `list` | no | Only return SMS entries that have a mobile processing error. Accepted values: `1`. |

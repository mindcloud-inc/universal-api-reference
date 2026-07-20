# List Inbound Messages with Leadspicker

Retrieves inbound messages from Leadspicker.

## Endpoint

- **Method:** `GET`
- **Path:** `/app/sb/api/inbound-messages`
- **Base URL:** `https://app.leadspicker.com`
- **Official documentation:** [List Inbound Messages](https://app.leadspicker.com/app/sb/api/docs#/Replies/apps_salesbooster_api_inbound_messages)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `search_query` | query | `string` | no | Search in person name, email, subject, and message content. |
| `custom_start_date` | query | `date` | no | Filter conversations received on or after this date (YYYY-MM-DD). |
| `custom_end_date` | query | `date` | no | Filter conversations received on or before this date (YYYY-MM-DD). |
| `browser_timezone` | query | `string` | no | IANA timezone name used for date boundaries. |

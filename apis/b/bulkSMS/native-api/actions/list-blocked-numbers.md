# List Blocked Numbers with BulkSMS

Retrieves blocked phone numbers from BulkSMS.

## Endpoint

- **Method:** `GET`
- **Path:** `/blocked-numbers`
- **Base URL:** `https://api.bulksms.com/v1`
- **Official documentation:** [List Blocked Numbers](https://www.bulksms.com/developer/json/v1/#tag/blocked-numbers/GET/blocked-numbers)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `min-id` | query | `number` | no | Return blocked-number records with an ID greater than or equal to this value. |

# Create Blocked Numbers with BulkSMS

Creates blocked phone numbers in BulkSMS.

## Endpoint

- **Method:** `POST`
- **Path:** `/blocked-numbers`
- **Base URL:** `https://api.bulksms.com/v1`
- **Official documentation:** [Create Blocked Numbers](https://www.bulksms.com/developer/json/v1/#tag/blocked-numbers/POST/blocked-numbers)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `blockedNumbers[]` | body | `array<object>` | yes | Array of blocked-number objects to create. Each item should include phoneNumber and can include description. |

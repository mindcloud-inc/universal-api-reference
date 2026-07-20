# Add Gmail Thread to Record with NetHunt CRM

Adds a Gmail thread to a NetHunt CRM record.

## Endpoint

- **Method:** `POST`
- **Path:** `/actions/link-gmail-thread/:recordId`
- **Base URL:** `https://nethunt.com/api/v1/zapier`
- **Official documentation:** [Add Gmail Thread to Record](https://nethunt.com/integration-api#link-gmail-thread)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `gmailThreadId` | body | `string` | yes | Gmail conversation ID to link with the record. |
| `recordId` | path | `string` | yes | Record ID to link with a Gmail thread. |

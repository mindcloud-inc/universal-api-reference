# Create Inbox Placement Test with EmailListVerify

Creates an inbox placement test in EmailListVerify.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/inboxPlacementTests`
- **Base URL:** `https://api.emaillistverify.com`
- **Official documentation:** [Create Inbox Placement Test](https://api.emaillistverify.com/api-doc#/Inbox%20Placement%20Test%20Endpoints/createPlacementTest)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | no | Optional name for the inbox placement test. |
| `webhookUrl` | body | `string` | no | Optional HTTP or HTTPS URL to receive placement-test results when complete. |

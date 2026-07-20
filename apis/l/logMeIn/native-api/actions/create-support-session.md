# Create Support Session with LogMeIn

Creates a new support session in LogMeIn.

## Endpoint

- **Method:** `POST`
- **Path:** `/goto-resolve/v1/sessions`
- **Base URL:** `https://api.goto.com`
- **Official documentation:** [Create Support Session](https://developer.goto.com/LogMeInResolve/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customerName` | body | `string` | yes | Required customer name for the support session. |
| `sessionType` | body | `number` | no | Optional numeric session type. |
| `supportType` | body | `number` | no | Optional numeric support type. |
| `webhooks[]` | body | `array<object>` | no | Optional webhook subscription entries for session updates. |

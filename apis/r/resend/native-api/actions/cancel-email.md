# Cancel Email with Resend

Cancels a scheduled email in Resend.

## Endpoint

- **Method:** `POST`
- **Path:** `/emails/:id/cancel`
- **Base URL:** `https://api.resend.com`
- **Official documentation:** [Cancel Email](https://resend.com/docs/api-reference/emails/cancel-email)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Email identifier to cancel. Maximum length: 0. |

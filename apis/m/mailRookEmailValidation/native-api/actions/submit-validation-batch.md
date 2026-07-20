# Submit Validation Batch with MailRook Email Validation

Submits a batch of email addresses for validation in MailRook.

## Endpoint

- **Method:** `POST`
- **Path:** `/validate/batch`
- **Base URL:** `https://api.mailrook.com/v1`
- **Official documentation:** [Submit Validation Batch](https://mailrook.com/docs/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `emails[]` | body | `array<string>` | yes | Array of email addresses to validate in one batch. |

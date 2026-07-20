# Verify Email (SMTP) with SuperSend

Verifies an email in SuperSend using SMTP.

## Endpoint

- **Method:** `POST`
- **Path:** `/email-validation/verify`
- **Base URL:** `https://api.supersend.io/v2`
- **Official documentation:** [Verify Email (SMTP)](https://docs.supersend.io/docs/email-validation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | — |
| `TeamId` | body | `string` | no | Optional team UUID for credit transaction attribution |

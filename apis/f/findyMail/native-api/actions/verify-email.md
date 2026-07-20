# Verify Email with FindyMail

Verifies an email address with FindyMail.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/verify`
- **Base URL:** `https://app.findymail.com`
- **Official documentation:** [Verify Email](https://www.findymail.com/api/email-verifier/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | Email address to verify for deliverability. |

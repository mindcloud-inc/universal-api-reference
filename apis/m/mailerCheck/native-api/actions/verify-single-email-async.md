# Verify Single Email Async with MailerCheck

Creates an asynchronous email verification request in MailerCheck.

## Endpoint

- **Method:** `POST`
- **Path:** `/check/single-async`
- **Base URL:** `https://app.mailercheck.com/api`
- **Official documentation:** [Verify Single Email Async](https://developers.mailercheck.com/email)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | Email address to verify asynchronously. |

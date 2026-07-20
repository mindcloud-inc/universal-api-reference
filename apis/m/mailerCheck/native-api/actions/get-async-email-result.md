# Get Async Email Result with MailerCheck

Retrieves an asynchronous email verification result from MailerCheck.

## Endpoint

- **Method:** `GET`
- **Path:** `/check/single-async/:verification_id`
- **Base URL:** `https://app.mailercheck.com/api`
- **Official documentation:** [Get Async Email Result](https://developers.mailercheck.com/email)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `verification_id` | path | `string` | yes | Async verification identifier returned by Verify Single Email Async. |

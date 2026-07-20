# Verify Email with Toofr

Queues an email verification in Toofr for callback delivery.

## Endpoint

- **Method:** `POST`
- **Path:** `/test_email.json`
- **Base URL:** `https://www.findemails.com/api/v1`
- **Official documentation:** [Verify Email](https://developer.findemails.com/?from=explinks.com)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `callback_url` | query | `string` | yes | Callback URL for asynchronous verification result delivery. |
| `email` | query | `string` | yes | Email address to verify. |

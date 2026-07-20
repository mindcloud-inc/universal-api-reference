# Queue Email Guess with Toofr

Queues an email guess in Toofr for callback delivery.

## Endpoint

- **Method:** `POST`
- **Path:** `/guess_email.json`
- **Base URL:** `https://www.findemails.com/api/v1`
- **Official documentation:** [Queue Email Guess](https://developer.findemails.com/?from=explinks.com)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `callback_url` | query | `string` | yes | Callback URL for asynchronous email guess result delivery. |
| `company_name` | query | `string` | yes | Person company name. |
| `first_name` | query | `string` | yes | Person first name. |
| `last_name` | query | `string` | yes | Person last name. |

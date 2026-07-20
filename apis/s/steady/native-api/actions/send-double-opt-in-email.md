# Send Double Opt-In Email with Steady

Sends a double opt-in email from Steady.

## Endpoint

- **Method:** `POST`
- **Path:** `/newsletter_subscribers/send_double_opt_in_email`
- **Base URL:** `https://steadyhq.com/api/v1`
- **Official documentation:** [Send Double Opt-In Email](https://developers.steadyhq.com/#post-newsletter_subscribers-send_double_opt_in_email)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | The email address of the prospective newsletter subscriber. |

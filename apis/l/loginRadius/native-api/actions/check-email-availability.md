# Check Email Availability with LoginRadius

Checks whether an email is available in LoginRadius.

## Endpoint

- **Method:** `GET`
- **Path:** `/identity/v2/auth/email`
- **Base URL:** `https://api.loginradius.com`
- **Official documentation:** [Check Email Availability](https://www.loginradius.com/docs/api/openapi/check-email-availability/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | query | `string` | yes | Email address to verify availability or retrieve the associated account. |
| `verificationtoken` | query | `string` | no | Verification token received in email. |
| `otp` | query | `string` | no | One-time passcode sent to the user's email. |
| `prevent_webhook` | query | `boolean` | no | When true, suppresses webhook events for this operation. |
| `uuid` | query | `string` | no | Email template UUID for welcome email flows. |
| `url` | query | `string` | no | URL to log the main domain in the database. |
| `welcomeemailtemplate` | query | `string` | no | Welcome email template name. |

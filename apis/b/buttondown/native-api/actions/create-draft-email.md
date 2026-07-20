# Create Draft Email with Buttondown

Creates a draft email in Buttondown.

## Endpoint

- **Method:** `POST`
- **Path:** `/emails`
- **Base URL:** `https://api.buttondown.com/v1`
- **Official documentation:** [Create Draft Email](https://docs.buttondown.com/api-emails-create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `subject` | body | `string` | yes | Draft email subject line. |
| `body` | body | `string` | yes | Draft email body content. |
| `description` | body | `string` | no | Internal description for the draft email. |
| `slug` | body | `string` | no | Optional draft slug. |
| `canonical_url` | body | `string` | no | Canonical URL for the email. |

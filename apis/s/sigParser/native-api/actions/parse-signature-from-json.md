# Parse Signature From JSON with SigParser

## Endpoint

- **Method:** `POST`
- **Path:** `/api/Parse/Email/Contact/JSON`
- **Base URL:** `https://ipaas.sigparser.com`
- **Official documentation:** [Parse Signature From JSON](https://ipaas.sigparser.com/v1#post-api-parse-email-contact-json)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `from_address` | body | `string` | yes | Email address that must match the sender signature. |
| `from_name` | body | `string` | no | Sender name shown in the message. |
| `subject` | body | `string` | no | Email subject line. |
| `htmlbody` | body | `string` | no | HTML body for the email, if available. |
| `plainbody` | body | `string` | no | Plain-text body for the email, if available. |
| `date` | body | `string` | no | Email sent date. |

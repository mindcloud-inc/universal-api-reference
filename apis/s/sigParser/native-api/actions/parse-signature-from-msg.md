# Parse Signature From MSG with SigParser

## Endpoint

- **Method:** `POST`
- **Path:** `/api/Parse/Email/Contact/MSG`
- **Base URL:** `https://ipaas.sigparser.com`
- **Official documentation:** [Parse Signature From MSG](https://ipaas.sigparser.com/v1#post-api-parse-email-contact-msg)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `msgFile` | body | `file` | yes | Upload the MSG file contents for the email to parse. |

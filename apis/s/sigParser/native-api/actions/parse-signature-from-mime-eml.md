# Parse Signature From MIME/EML with SigParser

## Endpoint

- **Method:** `POST`
- **Path:** `/api/Parse/Email/Contact/MIME`
- **Base URL:** `https://ipaas.sigparser.com`
- **Official documentation:** [Parse Signature From MIME/EML](https://ipaas.sigparser.com/v1#post-api-parse-email-contact-mime)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `mimeFile` | body | `file` | yes | Upload the MIME or EML file contents for the email to parse. |

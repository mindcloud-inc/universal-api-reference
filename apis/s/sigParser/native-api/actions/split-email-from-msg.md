# Split Email From MSG with SigParser

## Endpoint

- **Method:** `POST`
- **Path:** `/api/Parse/Email/Message/MSG`
- **Base URL:** `https://ipaas.sigparser.com`
- **Official documentation:** [Split Email From MSG](https://ipaas.sigparser.com/v1#post-api-parse-email-message-msg)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `msgFile` | body | `file` | yes | Upload the Outlook MSG file contents for the email to split. |

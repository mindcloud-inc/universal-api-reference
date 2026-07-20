# Add Suppressed Email with Retently

Creates a suppressed email entry in Retently.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/suppressions/emails`
- **Base URL:** `https://app.retently.com`
- **Official documentation:** [Add Suppressed Email](https://www.retently.com/api/#api-post-suppressions-emails)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | The email address to suppress; |
| `note` | body | `string` | no | An optional note explaining why the email was suppressed; |

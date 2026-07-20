# Create Campaign with SendMails

Creates a new campaign in SendMails.

## Endpoint

- **Method:** `POST`
- **Path:** `/campaigns`
- **Base URL:** `https://app.sendmails.io/api/v1`
- **Official documentation:** [Create Campaign](https://sendmails.io/docs/campaigns-apis-by-sendmails-io/#4-toc-title)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `list_uid` | query | `string` | yes | List UID. |
| `name` | query | `string` | yes | Campaign name. |
| `subject` | query | `string` | yes | Email subject. |
| `from_email` | query | `string` | yes | From email address. |
| `from_name` | query | `string` | yes | From name. |
| `reply_to` | query | `string` | yes | Reply-to email address. |
| `track_open` | query | `string` | no | Track email opens. |
| `track_click` | query | `string` | no | Track email clicks. |
| `sign_dkim` | query | `string` | no | Sign with DKIM. |
| `skip_failed_messages` | query | `string` | no | Skip failed messages. |

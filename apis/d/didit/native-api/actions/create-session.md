# Create Session with Didit

Creates a new verification session in Didit.

## Endpoint

- **Method:** `POST`
- **Path:** `https://verification.didit.me/v3/session/`
- **Base URL:** `https://verification.didit.me/v3`
- **Official documentation:** [Create Session](https://docs.didit.me/sessions-api/create-session)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `callback` | body | `string` | no | URL where Didit redirects the user after the session. |
| `callback_method` | body | `string` | no | Callback handling mode. |
| `language` | body | `string` | no | Preferred session language code. |
| `metadata` | body | `string` | no | Metadata string attached to the session. |
| `vendor_data` | body | `string` | no | Your external reference for the session. |
| `workflow_id` | body | `string` | yes | Workflow identifier configured in Didit. |

# Register New Email Webhook with gyfti

Registers a new email webhook in gyfti.

## Endpoint

- **Method:** `POST`
- **Path:** `/wf/new_hook_email/`
- **Base URL:** `https://app.gyfti.fr/api/1.1`
- **Official documentation:** [Register New Email Webhook](https://developer.gyfti.fr/retrieve-data-from-campaigns/new-email)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `hookUrl` | body | `string` | yes | Destination URL that gyfti should call when a new email event occurs. |
| `user` | body | `string` | yes | gyfti user email associated with the webhook registration. |

# Add Suppression with Zoho ZeptoMail

Adds a suppression list entry in Zoho ZeptoMail.

## Endpoint

- **Method:** `POST`
- **Path:** `suppressions/:type`
- **Base URL:** `https://api.zeptomail.com/v1.1`
- **Official documentation:** [Add Suppression](https://www.zoho.com/zeptomail/help/api/add-suppression-list.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `type` | path | `string` | yes | Suppression category to manage. |
| `action` | body | `string` | yes | Suppression action: reject, suppress, or suppress_tracking. |
| `values[0]` | body | `string` | yes | Email address or domain to suppress. |
| `description` | body | `string` | no | Reason for the suppression entry. |
| `mailagent_keys[0]` | body | `string` | no | Agent alias to apply the suppression to. |

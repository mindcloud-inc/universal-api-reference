# Update Lead with Nova

## Endpoint

- **Method:** `PUT`
- **Path:** `/rt/update/lead`
- **Base URL:** `https://app.n0va.com/v1/la`
- **Official documentation:** [Update Lead](https://app.n0va.com/documentation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `origin_crm_id` | body | `string` | yes | External CRM lead identifier used by Nova to locate the lead to update. |
| `phone_number_concatenated` | body | `string` | no | Updated lead phone number. |
| `firstname` | body | `string` | no | Updated lead first name. |
| `lastname` | body | `string` | no | Updated lead last name. |
| `email` | body | `string` | no | Updated lead email address. |
| `statut` | body | `string` | no | Updated Nova lead status label. |
| `assigned_to` | body | `string` | no | Updated Nova user ID assigned to the lead. |
| `commentaire` | body | `string` | no | Updated lead comment. |

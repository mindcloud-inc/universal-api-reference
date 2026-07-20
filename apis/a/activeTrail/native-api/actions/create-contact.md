# Create Contact with ActiveTrail

Creates a new contact in ActiveTrail.

## Endpoint

- **Method:** `POST`
- **Path:** `/contacts`
- **Base URL:** `https://webapi.mymarketing.co.il/api`
- **Official documentation:** [Create Contact](https://webapi.mymarketing.co.il/api/docs/and/Api/POST-api-contacts)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `anniversary` | body | `date` | no | Contact field. |
| `birthday` | body | `date` | no | Contact field. |
| `double_optin` | body | `string` | no | Double opt-in settings. |
| `email` | body | `string` | no | Required if SMS is null. |
| `first_name` | body | `string` | no | Contact field. |
| `last_name` | body | `string` | no | Contact field. |
| `sms` | body | `string` | no | Required if email is null. |
| `sms_status` | body | `string` | no | Choose the SMS status. |
| `status` | body | `string` | no | Choose the contact status. |
| `subscribe_ip` | body | `string` | no | The subscribe IP. |

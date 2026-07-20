# Add Contact to Group with ActiveTrail

Adds a contact to a group in ActiveTrail.

## Endpoint

- **Method:** `POST`
- **Path:** `/groups/:id/members`
- **Base URL:** `https://webapi.mymarketing.co.il/api`
- **Official documentation:** [Add Contact to Group](https://webapi.mymarketing.co.il/api/docs/and/Api/POST-api-groups-id-members)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `double_optin` | body | `string` | no | Double opt-in settings. |
| `email` | body | `string` | no | Required if SMS is null. |
| `first_name` | body | `string` | no | Contact field. |
| `id` | path | `number` | yes | Group id. Can be found using the account groups endpoint or in the UI. |
| `last_name` | body | `string` | no | Contact field. |
| `sms` | body | `string` | no | Required if email is null. |
| `sms_status` | body | `string` | no | Choose the SMS status. |
| `status` | body | `string` | no | Choose the contact status. |
| `subscribe_ip` | body | `string` | no | The subscribe IP. |

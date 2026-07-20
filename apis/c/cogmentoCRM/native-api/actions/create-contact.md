# Create Contact with Cogmento CRM

## Endpoint

- **Method:** `POST`
- **Path:** `/contacts/`
- **Base URL:** `https://api.freecrm.com/api/1`
- **Official documentation:** [Create Contact](https://api.cogmento.com/static/swagger/index.html#/Contacts/post_contacts_)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `first_name` | body | `string` | yes | First name of the contact. |
| `last_name` | body | `string` | yes | Last name of the contact. |
| `channels[]` | body | `array<object>` | no | Contact channels array, such as email or phone channel objects. |
| `description` | body | `string` | no | Description of the contact. |
| `tags[]` | body | `array<string>` | no | Tags associated with the contact. Send multiple values as a array. |
| `do_not_call` | body | `boolean` | no | Set true to mark the contact as do not call. |
| `do_not_text` | body | `boolean` | no | Set true to mark the contact as do not text. |
| `do_not_email` | body | `boolean` | no | Set true to mark the contact as do not email. |

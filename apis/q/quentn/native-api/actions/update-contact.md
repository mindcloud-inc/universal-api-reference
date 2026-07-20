# Update Contact with Quentn

## Endpoint

- **Method:** `PUT`
- **Path:** `/contact/:contact_id`
- **Base URL:** `https://tbg6y3.us-1.quentn.com/public/api/v1`
- **Official documentation:** [Update Contact](https://help.quentn.com/hc/en-150/articles/4517835330961-Contact-API)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contact_id` | path | `number` | yes | The numeric Quentn contact id to update. |
| `family_name` | body | `string` | no | Optional updated last name. |
| `first_name` | body | `string` | no | Optional updated first name. |
| `mail` | body | `string` | no | Optional updated email address. |

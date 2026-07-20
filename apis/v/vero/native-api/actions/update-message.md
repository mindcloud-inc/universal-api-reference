# Update Message with Vero

Updates an existing message in Vero.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/v4/messages/:id`
- **Base URL:** `https://api.getvero.com`
- **Official documentation:** [Update Message](https://help.getvero.com/api-reference/messages/update-an-email-message)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The message identifier. |
| `provider` | body | `string` | no | Optional message provider value. |
| `transactional` | body | `boolean` | no | Optional transactional flag. |
| `contents` | body | `object` | no | Optional message contents object. |

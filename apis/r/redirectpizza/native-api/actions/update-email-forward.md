# Update Email Forward with redirect.pizza

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/v1/email-forwards/{id}`
- **Base URL:** `https://redirect.pizza`
- **Official documentation:** [Update Email Forward](https://redirect.pizza/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | ID of the email forward to update. |
| `destination` | body | `string` | yes | Destination email address. |

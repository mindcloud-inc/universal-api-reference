# Trigger Email Callback with Salebot

## Endpoint

- **Method:** `POST`
- **Path:** `/email_callback`
- **Base URL:** `https://chatter.salebot.pro/api/{apiKey}`
- **Official documentation:** [Trigger Email Callback](https://docs.salebot.pro/rabota-s-api/api-konstruktora)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | no | Client display name. |
| `message` | body | `string` | no | Callback text to inject into the email bot flow. |
| `email` | body | `string` | yes | Customer email address. |
| `email_id_bot` | body | `string` | yes | Email address of the Salebot email bot. |
| `resume_bot` | body | `boolean` | no | Resume a paused bot before delivering the callback. |

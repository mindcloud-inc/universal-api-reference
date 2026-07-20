# Trigger Callback with Salebot

## Endpoint

- **Method:** `POST`
- **Path:** `/callback`
- **Base URL:** `https://chatter.salebot.pro/api/{apiKey}`
- **Official documentation:** [Trigger Callback](https://docs.salebot.pro/rabota-s-api/api-konstruktora)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `client_id` | body | `number` | no | Existing Salebot client ID. |
| `client_phone` | body | `string` | no | Phone number used to resolve the client before triggering the callback. |
| `client_email` | body | `string` | no | Email used to resolve the client before triggering the callback. |
| `message` | body | `string` | no | Callback text to inject into the bot flow. |
| `resume_bot` | body | `boolean` | no | Resume a paused bot before delivering the callback. |

# Identify User with Candu

Updates a user profile in Candu.

## Endpoint

- **Method:** `POST`
- **Path:** `/eventWebhook`
- **Base URL:** `https://api.candu.ai/api`
- **Official documentation:** [Identify User](https://developers.candu.ai/docs/get-data-into-candu-via-the-rest-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `userId` | body | `string` | yes | The user ID to identify. |
| `traits` | body | `object` | yes | User traits to store in Candu. |
| `timestamp` | body | `date` | no | Optional event timestamp. |

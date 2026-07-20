# Get Portal Token with SWELLEnterprise

Retrieves a portal token from SWELLEnterprise.

## Endpoint

- **Method:** `POST`
- **Path:** `/client-portal/token`
- **Base URL:** `https://dashboard.swellsystem.com/api/v1`
- **Official documentation:** [Get Portal Token](https://dashboard.swellsystem.com/docs#client-portal-POSTapi-v1-client-portal-token)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `type` | body | `string` | yes | The type: contact or company. |
| `id` | body | `number` | yes | The ID of the contact or company. |

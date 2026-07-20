# Create Session with Airtop

Creates a new session in Airtop.

## Endpoint

- **Method:** `POST`
- **Path:** `/sessions`
- **Base URL:** `https://api.airtop.ai/api/v1`
- **Official documentation:** [Create Session](https://docs.airtop.ai/api-reference/airtop-api/sessions/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `configuration.baseProfileId` | body | `string` | no | Base profile ID to clone when creating the session |
| `configuration.persistProfile` | body | `boolean` | no | Persist the session profile for later reuse |
| `configuration.timeoutMinutes` | body | `number` | no | Maximum session duration in minutes |

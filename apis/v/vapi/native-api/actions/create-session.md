# Create Session with Vapi

Creates a new session in Vapi.

## Endpoint

- **Method:** `POST`
- **Path:** `/session`
- **Base URL:** `https://api.vapi.ai`
- **Official documentation:** [Create Session](https://docs.vapi.ai/api-reference/sessions/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | no | This is a user-defined name for the session. Maximum length is 40 characters. |
| `status` | body | `string` | no | This is the current status of the session. Can be either 'active' or 'completed'. |
| `expirationSeconds` | body | `number` | no | Session expiration time in seconds. Defaults to 24 hours (86400 seconds) if not set. |
| `assistantId` | body | `string` | no | This is the ID of the assistant associated with this session. Use this when referencing an existing assistant. |
| `assistant` | body | `object` | no | — |
| `assistantOverrides` | body | `object` | no | — |
| `squadId` | body | `string` | no | This is the squad ID associated with this session. Use this when referencing an existing squad. |
| `squad` | body | `object` | no | — |
| `messages[]` | body | `array<object>` | no | This is an array of chat messages in the session. |
| `customer` | body | `object` | no | — |
| `customerId` | body | `string` | no | This is the customerId of the customer associated with this session. |
| `phoneNumberId` | body | `string` | no | This is the ID of the phone number associated with this session. |
| `phoneNumber` | body | `object` | no | — |

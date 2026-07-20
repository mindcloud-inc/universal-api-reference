# Create Production Applications with Bridge

Creates production applications in Bridge.

## Endpoint

- **Method:** `POST`
- **Path:** `/applications`
- **Base URL:** `https://api.bridgeapi.io/v3`
- **Official documentation:** [Create Production Applications](https://docs.bridgeapi.io/reference/createapplications)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `dashboard_user_email` | body | `string` | yes | The email of the dashboard user who will be the ADMIN of the application and receive the client ID and client secret |
| `applications[]` | body | `array<object>` | yes | — |

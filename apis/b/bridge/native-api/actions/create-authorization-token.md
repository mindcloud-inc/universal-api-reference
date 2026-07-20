# Create Authorization Token with Bridge

Creates a user authorization token in Bridge.

## Endpoint

- **Method:** `POST`
- **Path:** `/aggregation/authorization/token`
- **Base URL:** `https://api.bridgeapi.io/v3`
- **Official documentation:** [Create Authorization Token](https://docs.bridgeapi.io/reference/createuserauthtoken)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `user_uuid` | body | `string` | no | The user UUID |
| `external_user_id` | body | `string` | no | Your own user ID |

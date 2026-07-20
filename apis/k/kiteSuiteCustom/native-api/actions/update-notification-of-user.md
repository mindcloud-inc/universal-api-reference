# Update notification of user with Kite Suite

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/v1/notification/:id`
- **Base URL:** `https://api.kitesuite.com`
- **Official documentation:** [Update notification of user](https://api.kitesuite.com/swagger/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `body` | body | `object` | yes | Request body |
| `id` | path | `string` | no | Notification Id |
| `isSeen` | body | `boolean` | yes | — |

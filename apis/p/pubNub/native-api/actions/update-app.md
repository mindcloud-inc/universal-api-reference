# Update App with PubNub

Updates an existing app in PubNub.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/apps/:id`
- **Base URL:** `https://admin-api.pubnub.com/v2`
- **Official documentation:** [Update App](https://www.pubnub.com/docs/admin-api/update-an-app)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The PubNub app ID. |
| `name` | body | `string` | yes | The updated PubNub app name. |

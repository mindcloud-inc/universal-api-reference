# Update Authentication with eGain

Updates an existing authentication in eGain.

## Endpoint

- **Method:** `PUT`
- **Path:** `/authentications/:id`
- **Base URL:** `https://api.ai.egain.cloud/conversation/conversationmgr/v3`
- **Official documentation:** [Update Authentication](https://apidev.egain.com/apis/v3/conversation/conversationmgr/api-bundled/authentication/updateauthentication.md)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `basicAuth.password` | body | `string` | yes | Basic auth password. |
| `basicAuth.username` | body | `string` | yes | Basic auth username. |
| `id` | path | `string` | yes | Authentication ID. |
| `name` | body | `string` | yes | Authentication name. |
| `type` | body | `string` | yes | Authentication type. |

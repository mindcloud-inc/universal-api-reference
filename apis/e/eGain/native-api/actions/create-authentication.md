# Create Authentication with eGain

Creates a new authentication in eGain.

## Endpoint

- **Method:** `POST`
- **Path:** `/authentications`
- **Base URL:** `https://api.ai.egain.cloud/conversation/conversationmgr/v3`
- **Official documentation:** [Create Authentication](https://apidev.egain.com/apis/v3/conversation/conversationmgr/api-bundled/authentication/createauthentication.md)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `basicAuth.password` | body | `string` | yes | Basic auth password. |
| `basicAuth.username` | body | `string` | yes | Basic auth username. |
| `name` | body | `string` | yes | Authentication name. |
| `type` | body | `string` | yes | Authentication type. |

# Create Client Application with eGain

Creates a new client application in eGain.

## Endpoint

- **Method:** `POST`
- **Path:** `/clientapplications`
- **Base URL:** `https://api.ai.egain.cloud/conversation/conversationmgr/v3`
- **Official documentation:** [Create Client Application](https://apidev.egain.com/api-catalog/conversation-conversationmgr/api-bundled/operation/createClientApplication/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `active` | body | `boolean` | yes | Whether the client application is active. |
| `description` | body | `string` | no | Client application description. |
| `name` | body | `string` | yes | Client application name. |
| `roles[0].callback` | body | `string` | yes | Role callback URL. |
| `roles[0].name` | body | `string` | yes | Role name. |
| `roles[0].notificationEmail` | body | `string` | yes | Role notification email. |
| `roles[0].version` | body | `string` | yes | Role version. |

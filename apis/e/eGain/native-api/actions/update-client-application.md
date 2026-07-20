# Update Client Application with eGain

Updates an existing client application in eGain.

## Endpoint

- **Method:** `PUT`
- **Path:** `/clientapplications/:id`
- **Base URL:** `https://api.ai.egain.cloud/conversation/conversationmgr/v3`
- **Official documentation:** [Update Client Application](https://apidev.egain.com/api-catalog/conversation-conversationmgr/api-bundled/operation/updateClientApplication/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `active` | body | `boolean` | yes | Whether the client application is active. |
| `description` | body | `string` | no | Client application description. |
| `id` | path | `string` | yes | Client application ID. |
| `name` | body | `string` | yes | Client application name. |
| `roles[0].callback` | body | `string` | yes | Role callback URL. |
| `roles[0].name` | body | `string` | yes | Role name. |
| `roles[0].notificationEmail` | body | `string` | yes | Role notification email. |
| `roles[0].version` | body | `string` | yes | Role version. |

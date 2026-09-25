# Create Group with Microsoft Entra

## Endpoint

- **Method:** `POST`
- **Path:** `/groups`
- **Base URL:** `https://graph.microsoft.com/v1.0`
- **Official documentation:** [Create Group](https://learn.microsoft.com/en-us/graph/api/group-post-groups?view=graph-rest-1.0)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `displayName` | body | `string` | yes | Maximum length: 256. |
| `mailEnabled` | body | `boolean` | yes | — |
| `mailNickname` | body | `string` | yes | Maximum length: 64. |
| `securityEnabled` | body | `boolean` | yes | — |
| `description` | body | `string` | no | — |
| `groupTypes[]` | body | `array<string>` | no | Use Unified for a Microsoft 365 group; leave empty for an assigned security group. Dynamic groups require additional configuration. |
| `members@odata.bind[]` | body | `array<string>` | no | Full Microsoft Graph resource URLs, such as https://graph.microsoft.com/v1.0/users/{id}. |
| `owners@odata.bind[]` | body | `array<string>` | no | Full Microsoft Graph resource URLs, such as https://graph.microsoft.com/v1.0/users/{id}. |

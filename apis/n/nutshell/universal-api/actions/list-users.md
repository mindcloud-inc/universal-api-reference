# Nutshell: List Users

Retrieves users from Nutshell.

```
GET https://connect.mindcloud.co/v1/universal/nutshell/latest/actions/list-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nutshell `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nutshell/latest/actions/list-users?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nutshell/latest/actions/list-users?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "agentStatus": "string",
      "autoPresenceEnabled": true,
      "avatarUrl": "https://example.com",
      "canAccessEmailMarketing": true,
      "emails": [
        "ava@example.com"
      ],
      "firstName": "Ava",
      "hasDisabledShortcuts": true,
      "hasSetPassword": true,
      "id": "string",
      "initials": "string",
      "isAdministrator": true,
      "isAgent": true,
      "isAircallEnabledForUser": true,
      "isEnabled": true,
      "isHiddenFromFilters": true,
      "isMainSidebarCollapsed": true,
      "isRecentlyAdded": true,
      "isViewingRestricted": true,
      "modifiedTime": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "permissions": {
        "canAccessBilling": true,
        "canAccessCrm": true,
        "canAccessFullCampaigns": true,
        "canAccessMarketing": true,
        "canAccessSetup": true,
        "canAssignEntities": true,
        "canBulkEdit": true,
        "canDeleteEntities": true,
        "canExport": true,
        "canImport": true,
        "canManageEmailTemplates": true,
        "canMergeEntities": true,
        "canUseInbox": true,
        "canUseOrTryInbox": true,
        "canUsePeopleIQ": true,
        "canUseProspectorIQ": true,
        "canUseSalesDocuments": true,
        "canUseSms": true,
        "canViewSharedEmails": true
      },
      "phonecallerType": "string",
      "shouldShowExploreAttentionBadge": true,
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `agentStatus` | string |  |
| `autoPresenceEnabled` | boolean |  |
| `avatarUrl` | string |  |
| `canAccessEmailMarketing` | boolean |  |
| `emails[]` | string |  |
| `firstName` | string |  |
| `hasDisabledShortcuts` | boolean |  |
| `hasSetPassword` | boolean |  |
| `id` | string |  |
| `initials` | string |  |
| `isAdministrator` | boolean |  |
| `isAgent` | boolean |  |
| `isAircallEnabledForUser` | boolean |  |
| `isEnabled` | boolean |  |
| `isHiddenFromFilters` | boolean |  |
| `isMainSidebarCollapsed` | boolean |  |
| `isRecentlyAdded` | boolean |  |
| `isViewingRestricted` | boolean |  |
| `modifiedTime` | date |  |
| `name` | string |  |
| `permissions.canAccessBilling` | boolean |  |
| `permissions.canAccessCrm` | boolean |  |
| `permissions.canAccessFullCampaigns` | boolean |  |
| `permissions.canAccessMarketing` | boolean |  |
| `permissions.canAccessSetup` | boolean |  |
| `permissions.canAssignEntities` | boolean |  |
| `permissions.canBulkEdit` | boolean |  |
| `permissions.canDeleteEntities` | boolean |  |
| `permissions.canExport` | boolean |  |
| `permissions.canImport` | boolean |  |
| `permissions.canManageEmailTemplates` | boolean |  |
| `permissions.canMergeEntities` | boolean |  |
| `permissions.canUseInbox` | boolean |  |
| `permissions.canUseOrTryInbox` | boolean |  |
| `permissions.canUsePeopleIQ` | boolean |  |
| `permissions.canUseProspectorIQ` | boolean |  |
| `permissions.canUseSalesDocuments` | boolean |  |
| `permissions.canUseSms` | boolean |  |
| `permissions.canViewSharedEmails` | boolean |  |
| `phonecallerType` | string |  |
| `shouldShowExploreAttentionBadge` | boolean |  |
| `type` | string |  |

## Native endpoint

Through the native Nutshell API, this operation is `GET /users` (base URL `https://app.nutshell.com/rest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-users.md) for the provider-specific parameters and requirements.


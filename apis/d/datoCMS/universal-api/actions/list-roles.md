# DatoCMS: List Roles



```
GET https://connect.mindcloud.co/v1/universal/datoCMS/latest/actions/list-roles
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DatoCMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/datoCMS/latest/actions/list-roles?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/datoCMS/latest/actions/list-roles?${params}`, {
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
      "attributes": {
        "canAccessAuditLog": true,
        "canAccessBuildEventsLog": true,
        "canAccessSearchIndexEventsLog": true,
        "canEditEnvironment": true,
        "canEditFavicon": true,
        "canEditSchema": true,
        "canEditSite": true,
        "canManageAccessTokens": true,
        "canManageBuildTriggers": true,
        "canManageEnvironments": true,
        "canManageMenu": true,
        "canManageSearchIndexes": true,
        "canManageSharedFilters": true,
        "canManageSso": true,
        "canManageUploadCollections": true,
        "canManageUsers": true,
        "canManageWebhooks": true,
        "canManageWorkflows": true,
        "canPerformSiteSearch": true,
        "canPromoteEnvironments": true,
        "environmentsAccess": "string",
        "name": "Ava Chen",
        "positiveBuildTriggerPermissions": [
          {
            "buildTrigger": "string"
          }
        ],
        "positiveItemTypePermissions": [
          {
            "action": "string",
            "environment": "string",
            "itemType": "string",
            "locale": "string",
            "localizationScope": "string",
            "onCreator": "string",
            "onStage": "string",
            "toStage": "string",
            "workflow": "string"
          }
        ],
        "positiveUploadPermissions": [
          {
            "action": "string",
            "environment": "string",
            "locale": "string",
            "localizationScope": "string",
            "moveToUploadCollection": "string",
            "onCreator": "string",
            "uploadCollection": "string"
          }
        ]
      },
      "id": "string",
      "meta": {
        "finalPermissions": {
          "canAccessAuditLog": true,
          "canAccessBuildEventsLog": true,
          "canAccessSearchIndexEventsLog": true,
          "canEditEnvironment": true,
          "canEditFavicon": true,
          "canEditSchema": true,
          "canEditSite": true,
          "canManageAccessTokens": true,
          "canManageBuildTriggers": true,
          "canManageEnvironments": true,
          "canManageMenu": true,
          "canManageSearchIndexes": true,
          "canManageSharedFilters": true,
          "canManageSso": true,
          "canManageUploadCollections": true,
          "canManageUsers": true,
          "canManageWebhooks": true,
          "canManageWorkflows": true,
          "canPerformSiteSearch": true,
          "canPromoteEnvironments": true,
          "environmentsAccess": "string",
          "positiveBuildTriggerPermissions": [
            {
              "buildTrigger": "string"
            }
          ],
          "positiveItemTypePermissions": [
            {
              "action": "string",
              "environment": "string",
              "itemType": "string",
              "locale": "string",
              "localizationScope": "string",
              "onCreator": "string",
              "onStage": "string",
              "toStage": "string",
              "workflow": "string"
            }
          ],
          "positiveUploadPermissions": [
            {
              "action": "string",
              "environment": "string",
              "locale": "string",
              "localizationScope": "string",
              "moveToUploadCollection": "string",
              "onCreator": "string",
              "uploadCollection": "string"
            }
          ]
        }
      },
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attributes.canAccessAuditLog` | boolean |  |
| `attributes.canAccessBuildEventsLog` | boolean |  |
| `attributes.canAccessSearchIndexEventsLog` | boolean |  |
| `attributes.canEditEnvironment` | boolean |  |
| `attributes.canEditFavicon` | boolean |  |
| `attributes.canEditSchema` | boolean |  |
| `attributes.canEditSite` | boolean |  |
| `attributes.canManageAccessTokens` | boolean |  |
| `attributes.canManageBuildTriggers` | boolean |  |
| `attributes.canManageEnvironments` | boolean |  |
| `attributes.canManageMenu` | boolean |  |
| `attributes.canManageSearchIndexes` | boolean |  |
| `attributes.canManageSharedFilters` | boolean |  |
| `attributes.canManageSso` | boolean |  |
| `attributes.canManageUploadCollections` | boolean |  |
| `attributes.canManageUsers` | boolean |  |
| `attributes.canManageWebhooks` | boolean |  |
| `attributes.canManageWorkflows` | boolean |  |
| `attributes.canPerformSiteSearch` | boolean |  |
| `attributes.canPromoteEnvironments` | boolean |  |
| `attributes.environmentsAccess` | string |  |
| `attributes.name` | string |  |
| `attributes.positiveBuildTriggerPermissions[].buildTrigger` | string |  |
| `attributes.positiveItemTypePermissions[].action` | string |  |
| `attributes.positiveItemTypePermissions[].environment` | string |  |
| `attributes.positiveItemTypePermissions[].itemType` | string |  |
| `attributes.positiveItemTypePermissions[].locale` | string |  |
| `attributes.positiveItemTypePermissions[].localizationScope` | string |  |
| `attributes.positiveItemTypePermissions[].onCreator` | string |  |
| `attributes.positiveItemTypePermissions[].onStage` | string |  |
| `attributes.positiveItemTypePermissions[].toStage` | string |  |
| `attributes.positiveItemTypePermissions[].workflow` | string |  |
| `attributes.positiveUploadPermissions[].action` | string |  |
| `attributes.positiveUploadPermissions[].environment` | string |  |
| `attributes.positiveUploadPermissions[].locale` | string |  |
| `attributes.positiveUploadPermissions[].localizationScope` | string |  |
| `attributes.positiveUploadPermissions[].moveToUploadCollection` | string |  |
| `attributes.positiveUploadPermissions[].onCreator` | string |  |
| `attributes.positiveUploadPermissions[].uploadCollection` | string |  |
| `id` | string |  |
| `meta.finalPermissions.canAccessAuditLog` | boolean |  |
| `meta.finalPermissions.canAccessBuildEventsLog` | boolean |  |
| `meta.finalPermissions.canAccessSearchIndexEventsLog` | boolean |  |
| `meta.finalPermissions.canEditEnvironment` | boolean |  |
| `meta.finalPermissions.canEditFavicon` | boolean |  |
| `meta.finalPermissions.canEditSchema` | boolean |  |
| `meta.finalPermissions.canEditSite` | boolean |  |
| `meta.finalPermissions.canManageAccessTokens` | boolean |  |
| `meta.finalPermissions.canManageBuildTriggers` | boolean |  |
| `meta.finalPermissions.canManageEnvironments` | boolean |  |
| `meta.finalPermissions.canManageMenu` | boolean |  |
| `meta.finalPermissions.canManageSearchIndexes` | boolean |  |
| `meta.finalPermissions.canManageSharedFilters` | boolean |  |
| `meta.finalPermissions.canManageSso` | boolean |  |
| `meta.finalPermissions.canManageUploadCollections` | boolean |  |
| `meta.finalPermissions.canManageUsers` | boolean |  |
| `meta.finalPermissions.canManageWebhooks` | boolean |  |
| `meta.finalPermissions.canManageWorkflows` | boolean |  |
| `meta.finalPermissions.canPerformSiteSearch` | boolean |  |
| `meta.finalPermissions.canPromoteEnvironments` | boolean |  |
| `meta.finalPermissions.environmentsAccess` | string |  |
| `meta.finalPermissions.positiveBuildTriggerPermissions[].buildTrigger` | string |  |
| `meta.finalPermissions.positiveItemTypePermissions[].action` | string |  |
| `meta.finalPermissions.positiveItemTypePermissions[].environment` | string |  |
| `meta.finalPermissions.positiveItemTypePermissions[].itemType` | string |  |
| `meta.finalPermissions.positiveItemTypePermissions[].locale` | string |  |
| `meta.finalPermissions.positiveItemTypePermissions[].localizationScope` | string |  |
| `meta.finalPermissions.positiveItemTypePermissions[].onCreator` | string |  |
| `meta.finalPermissions.positiveItemTypePermissions[].onStage` | string |  |
| `meta.finalPermissions.positiveItemTypePermissions[].toStage` | string |  |
| `meta.finalPermissions.positiveItemTypePermissions[].workflow` | string |  |
| `meta.finalPermissions.positiveUploadPermissions[].action` | string |  |
| `meta.finalPermissions.positiveUploadPermissions[].environment` | string |  |
| `meta.finalPermissions.positiveUploadPermissions[].locale` | string |  |
| `meta.finalPermissions.positiveUploadPermissions[].localizationScope` | string |  |
| `meta.finalPermissions.positiveUploadPermissions[].moveToUploadCollection` | string |  |
| `meta.finalPermissions.positiveUploadPermissions[].onCreator` | string |  |
| `meta.finalPermissions.positiveUploadPermissions[].uploadCollection` | string |  |
| `type` | string |  |

## Native endpoint

Through the native DatoCMS API, this operation is `GET /roles` (base URL `https://site-api.datocms.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-roles.md) for the provider-specific parameters and requirements.


# Sumo Logic: List Apps

Retrieves apps from the Sumo Logic App Catalog.

```
GET https://connect.mindcloud.co/v1/universal/sumoLogic/latest/actions/list-apps
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sumo Logic `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sumoLogic/latest/actions/list-apps?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sumoLogic/latest/actions/list-apps?${params}`, {
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
      "appDefinition": {
        "appVersion": "string",
        "contentId": "string",
        "manifestVersion": "string",
        "name": "Ava Chen",
        "preview": true,
        "uuid": "string"
      },
      "appManifest": {
        "accountTypes": [
          "string"
        ],
        "author": "string",
        "authorWebsite": "string",
        "categories": [
          "string"
        ],
        "communityURL": "https://example.com",
        "contentType": "string",
        "description": "string",
        "family": "string",
        "helpDocIdMap": "string",
        "helpURL": "https://example.com",
        "hoverText": "string",
        "iconURL": "https://example.com",
        "installationInstructions": "string",
        "parameters": [
          {
            "dataSourceType": "string",
            "description": "string",
            "example": "string",
            "label": "string",
            "parameterId": "string",
            "parameterType": "string"
          }
        ],
        "requirements": [
          "string"
        ],
        "requiresInstallationInstructions": true,
        "screenshotURLs": [
          "https://example.com"
        ]
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `appDefinition.appVersion` | string |  |
| `appDefinition.contentId` | string |  |
| `appDefinition.manifestVersion` | string |  |
| `appDefinition.name` | string |  |
| `appDefinition.preview` | boolean |  |
| `appDefinition.uuid` | string |  |
| `appManifest.accountTypes[]` | string |  |
| `appManifest.author` | string |  |
| `appManifest.authorWebsite` | string |  |
| `appManifest.categories[]` | string |  |
| `appManifest.communityURL` | string |  |
| `appManifest.contentType` | string |  |
| `appManifest.description` | string |  |
| `appManifest.family` | string |  |
| `appManifest.helpDocIdMap` | string |  |
| `appManifest.helpURL` | string |  |
| `appManifest.hoverText` | string |  |
| `appManifest.iconURL` | string |  |
| `appManifest.installationInstructions` | string |  |
| `appManifest.parameters[].dataSourceType` | string |  |
| `appManifest.parameters[].description` | string |  |
| `appManifest.parameters[].example` | string |  |
| `appManifest.parameters[].label` | string |  |
| `appManifest.parameters[].parameterId` | string |  |
| `appManifest.parameters[].parameterType` | string |  |
| `appManifest.requirements[]` | string |  |
| `appManifest.requiresInstallationInstructions` | boolean |  |
| `appManifest.screenshotURLs[]` | string |  |

## Native endpoint

Through the native Sumo Logic API, this operation is `GET /v1/apps` (base URL `https://api.sumologic.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-apps.md) for the provider-specific parameters and requirements.


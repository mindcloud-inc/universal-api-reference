# Nucleus One: Get Project Settings

Retrieves project settings from Nucleus One.

```
GET https://connect.mindcloud.co/v1/universal/nucleusOne/latest/actions/get-project-settings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nucleus One `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nucleusOne/latest/actions/get-project-settings?connectionId=$CONNECTION_ID&organizationId=Enter%20organizationId&projectId=Enter%20projectId" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "organizationId": "Enter organizationId",
  "projectId": "Enter projectId"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nucleusOne/latest/actions/get-project-settings?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `organizationId` | string | yes | Organization ID Example: `Enter organizationId`. |
| `projectId` | string | yes | Project ID Example: `Enter projectId`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "$schema": "string",
      "AllowPublicDocumentFolders": true,
      "DocumentRootLabel": "string",
      "ProjectAccess": {},
      "ProjectID": "string",
      "ProjectName": "Ava Chen",
      "PublicCardActionBarBackgroundColor": "string",
      "PublicDefaultBackgroundColor": "string",
      "PublicFolderIconURL": "https://example.com",
      "PublicFontFamily": "string",
      "PublicFontURL": "https://example.com",
      "PublicPaneBackgroundColor": "string",
      "PublicPaperBackgroundColor": "string",
      "PublicPrimaryAccentColor": "string",
      "PublicPrimaryColor": "string",
      "PublicSecondaryAccentColor": "string",
      "PublicSecondaryColor": "string",
      "PublicToolBarBackgroundColor": "string",
      "PublicTreeNodeHighlightBackgroundColor": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `$schema` | string |  |
| `AllowPublicDocumentFolders` | boolean |  |
| `DocumentRootLabel` | string |  |
| `ProjectAccess` | object |  |
| `ProjectID` | string |  |
| `ProjectName` | string |  |
| `PublicCardActionBarBackgroundColor` | string |  |
| `PublicDefaultBackgroundColor` | string |  |
| `PublicFolderIconURL` | string |  |
| `PublicFontFamily` | string |  |
| `PublicFontURL` | string |  |
| `PublicPaneBackgroundColor` | string |  |
| `PublicPaperBackgroundColor` | string |  |
| `PublicPrimaryAccentColor` | string |  |
| `PublicPrimaryColor` | string |  |
| `PublicSecondaryAccentColor` | string |  |
| `PublicSecondaryColor` | string |  |
| `PublicToolBarBackgroundColor` | string |  |
| `PublicTreeNodeHighlightBackgroundColor` | string |  |

## Native endpoint

Through the native Nucleus One API, this operation is `GET /organizations/:organizationId/projects/:projectId/settings` (base URL `https://client-api.nucleus.one/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-project-settings.md) for the provider-specific parameters and requirements.


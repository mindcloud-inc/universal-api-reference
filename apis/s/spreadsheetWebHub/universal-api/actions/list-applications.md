# SpreadsheetWeb Hub: List Applications

Retrieves applications from a SpreadsheetWeb Hub workspace.

```
GET https://connect.mindcloud.co/v1/universal/spreadsheetWebHub/latest/actions/list-applications
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SpreadsheetWeb Hub `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/spreadsheetWebHub/latest/actions/list-applications?connectionId=$CONNECTION_ID&limit=25&offset=0&workspaceId=string&onlyPublishedWithDatabases=true" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "workspaceId": "string",
  "onlyPublishedWithDatabases": "true"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/spreadsheetWebHub/latest/actions/list-applications?${params}`, {
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
| `workspaceId` | string | yes | The target workspace identifier. |
| `onlyPublishedWithDatabases` | boolean | yes | When true, list only applications that have databases and published transactions. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accessCount": 1,
      "applicationId": "string",
      "creationDate": "2026-05-07T12:00:00.000Z",
      "enableInteractiveMode": true,
      "imageFileId": "string",
      "modificationDate": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "slug": "string",
      "tagRelationships": [
        [
          {}
        ]
      ],
      "workspaceId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accessCount` | number |  |
| `applicationId` | string |  |
| `creationDate` | date |  |
| `enableInteractiveMode` | boolean |  |
| `imageFileId` | string |  |
| `modificationDate` | date |  |
| `name` | string |  |
| `slug` | string |  |
| `tagRelationships[]` | array<object> |  |
| `tagRelationships[].applicationId` | string |  |
| `tagRelationships[].dashboardId` | string |  |
| `tagRelationships[].relationshipType` | number |  |
| `tagRelationships[].tagId` | string |  |
| `tagRelationships[].tagRelationshipId` | string |  |
| `tagRelationships[].userId` | string |  |
| `tagRelationships[].workspaceId` | string |  |
| `workspaceId` | string |  |

## Native endpoint

Through the native SpreadsheetWeb Hub API, this operation is `POST /applications/list/:workspaceId/:onlyPublishedWithDatabases` (base URL `https://api.spreadsheetweb.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-applications.md) for the provider-specific parameters and requirements.


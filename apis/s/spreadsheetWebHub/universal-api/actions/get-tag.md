# SpreadsheetWeb Hub: Get Tag

Retrieves a tag from SpreadsheetWeb Hub.

```
GET https://connect.mindcloud.co/v1/universal/spreadsheetWebHub/latest/actions/get-tag
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SpreadsheetWeb Hub `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/spreadsheetWebHub/latest/actions/get-tag?connectionId=$CONNECTION_ID&tagId=string&workspaceId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "tagId": "string",
  "workspaceId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/spreadsheetWebHub/latest/actions/get-tag?${params}`, {
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
| `tagId` | string | yes | SpreadsheetWeb tag UUID. |
| `workspaceId` | string | yes | SpreadsheetWeb workspace UUID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "color": "string",
      "creationDate": "2026-05-07T12:00:00.000Z",
      "icon": 1,
      "isOutline": true,
      "isRounded": true,
      "modificationDate": "2026-05-07T12:00:00.000Z",
      "style": 1,
      "tagId": "string",
      "tagRelationships": [
        [
          {}
        ]
      ],
      "text": "string",
      "textColor": "string",
      "type": 1,
      "workspaceId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `color` | string |  |
| `creationDate` | date |  |
| `icon` | number |  |
| `isOutline` | boolean |  |
| `isRounded` | boolean |  |
| `modificationDate` | date |  |
| `style` | number |  |
| `tagId` | string |  |
| `tagRelationships[]` | array<object> |  |
| `tagRelationships[].applicationId` | string |  |
| `tagRelationships[].dashboardId` | string |  |
| `tagRelationships[].relationshipType` | number |  |
| `tagRelationships[].tagId` | string |  |
| `tagRelationships[].tagRelationshipId` | string |  |
| `tagRelationships[].userId` | string |  |
| `tagRelationships[].workspaceId` | string |  |
| `text` | string |  |
| `textColor` | string |  |
| `type` | number |  |
| `workspaceId` | string |  |

## Native endpoint

Through the native SpreadsheetWeb Hub API, this operation is `GET /tags/get/:tagId/:workspaceId` (base URL `https://api.spreadsheetweb.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-tag.md) for the provider-specific parameters and requirements.


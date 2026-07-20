# SpreadsheetWeb Hub: Update Tag

Updates an existing tag in SpreadsheetWeb Hub.

```
PUT https://connect.mindcloud.co/v1/universal/spreadsheetWebHub/latest/actions/update-tag
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SpreadsheetWeb Hub `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/spreadsheetWebHub/latest/actions/update-tag" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "request.text": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/spreadsheetWebHub/latest/actions/update-tag', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "request.text": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `request` | object | no | Primary request payload. |
| `request.workspaceId` | string | no | SpreadsheetWeb workspace UUID. |
| `request.tagId` | string | no | SpreadsheetWeb tag UUID. |
| `request.text` | string | yes | Tag label text. |

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

Through the native SpreadsheetWeb Hub API, this operation is `POST /tags/edit` (base URL `https://api.spreadsheetweb.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-tag.md) for the provider-specific parameters and requirements.


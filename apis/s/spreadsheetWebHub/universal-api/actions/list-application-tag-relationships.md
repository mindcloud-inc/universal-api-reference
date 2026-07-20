# SpreadsheetWeb Hub: List Application Tag Relationships

Retrieves application tag relationships from SpreadsheetWeb Hub.

```
GET https://connect.mindcloud.co/v1/universal/spreadsheetWebHub/latest/actions/list-application-tag-relationships
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SpreadsheetWeb Hub `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/spreadsheetWebHub/latest/actions/list-application-tag-relationships?connectionId=$CONNECTION_ID&applicationId=string&workspaceId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "applicationId": "string",
  "workspaceId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/spreadsheetWebHub/latest/actions/list-application-tag-relationships?${params}`, {
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
| `applicationId` | string | yes | The target application identifier. |
| `workspaceId` | string | yes | The target workspace identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "applicationId": "string",
      "dashboardId": "string",
      "relationshipType": 1,
      "tagId": "string",
      "tagRelationshipId": "string",
      "userId": "string",
      "workspaceId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `applicationId` | string |  |
| `dashboardId` | string |  |
| `relationshipType` | number |  |
| `tagId` | string |  |
| `tagRelationshipId` | string |  |
| `userId` | string |  |
| `workspaceId` | string |  |

## Native endpoint

Through the native SpreadsheetWeb Hub API, this operation is `GET /applications/gettagrelationships/:applicationId/:workspaceId` (base URL `https://api.spreadsheetweb.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-application-tag-relationships.md) for the provider-specific parameters and requirements.


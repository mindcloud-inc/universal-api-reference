# SpreadsheetWeb Hub: Get User

Retrieves a user from SpreadsheetWeb Hub.

```
GET https://connect.mindcloud.co/v1/universal/spreadsheetWebHub/latest/actions/get-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SpreadsheetWeb Hub `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/spreadsheetWebHub/latest/actions/get-user?connectionId=$CONNECTION_ID&workspaceId=string&userId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "workspaceId": "string",
  "userId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/spreadsheetWebHub/latest/actions/get-user?${params}`, {
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
| `workspaceId` | string | yes | SpreadsheetWeb workspace UUID. |
| `userId` | string | yes | SpreadsheetWeb user UUID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "creationDate": "2026-05-07T12:00:00.000Z",
      "defaultDashboardId": "string",
      "isOwner": true,
      "isSupportAccess": true,
      "lastAppliedTemplateId": "string",
      "modificationDate": "2026-05-07T12:00:00.000Z",
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
| `creationDate` | date |  |
| `defaultDashboardId` | string |  |
| `isOwner` | boolean |  |
| `isSupportAccess` | boolean |  |
| `lastAppliedTemplateId` | string |  |
| `modificationDate` | date |  |
| `userId` | string |  |
| `workspaceId` | string |  |

## Native endpoint

Through the native SpreadsheetWeb Hub API, this operation is `GET /users/get/:workspaceId/:userId` (base URL `https://api.spreadsheetweb.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user.md) for the provider-specific parameters and requirements.


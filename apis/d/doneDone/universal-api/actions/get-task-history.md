# DoneDone: Get Task History

Retrieves task history from DoneDone.

```
GET https://connect.mindcloud.co/v1/universal/doneDone/latest/actions/get-task-history
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DoneDone `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/doneDone/latest/actions/get-task-history?connectionId=$CONNECTION_ID&accountId=1&projectId=1&taskId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "accountId": "1",
  "projectId": "1",
  "taskId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/doneDone/latest/actions/get-task-history?${params}`, {
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
| `accountId` | number | yes | DoneDone account ID. |
| `projectId` | number | yes | DoneDone internal project ID. |
| `taskId` | number | yes | DoneDone task ID. |
| `sort` | string | no | Sort direction for task history. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "action": "string",
      "canEdit": true,
      "createdOn": "2026-05-07T12:00:00.000Z",
      "createdOnEpochTime": "2026-05-07T12:00:00.000Z",
      "creator": {
        "email": "ava@example.com",
        "id": 1,
        "isGuest": true,
        "name": "Ava Chen",
        "photoUrl": "https://example.com"
      },
      "description": "string",
      "hasViewed": true,
      "id": 1,
      "isEdited": true,
      "taskEventTypeID": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `action` | string |  |
| `canEdit` | boolean |  |
| `createdOn` | date |  |
| `createdOnEpochTime` | date |  |
| `creator.email` | string |  |
| `creator.id` | number |  |
| `creator.isGuest` | boolean |  |
| `creator.name` | string |  |
| `creator.photoUrl` | string |  |
| `description` | string |  |
| `hasViewed` | boolean |  |
| `id` | number |  |
| `isEdited` | boolean |  |
| `taskEventTypeID` | number |  |

## Native endpoint

Through the native DoneDone API, this operation is `GET /:account_id/internal-projects/:internal_project_id/tasks/:task_id/history` (base URL `https://2.donedone.com/public-api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-task-history.md) for the provider-specific parameters and requirements.


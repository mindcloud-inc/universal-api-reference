# ITM Platform: List Task Team



```
GET https://connect.mindcloud.co/v1/universal/iTMPlatform/latest/actions/list-task-team
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ITM Platform `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/iTMPlatform/latest/actions/list-task-team?connectionId=$CONNECTION_ID&projectId=string&taskId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "string",
  "taskId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/iTMPlatform/latest/actions/list-task-team?${params}`, {
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
| `projectId` | string | yes | The ITM Platform project ID. |
| `taskId` | string | yes | The ITM Platform task ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "firstName": "Ava",
      "lastName": "Chen",
      "serviceAlias": "string",
      "srNo": "string",
      "taskUserId": 1,
      "userId": 1,
      "userId1": 1,
      "userName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `firstName` | string |  |
| `lastName` | string |  |
| `serviceAlias` | string |  |
| `srNo` | string |  |
| `taskUserId` | number |  |
| `userId` | number |  |
| `userId1` | number |  |
| `userName` | string |  |

## Native endpoint

Through the native ITM Platform API, this operation is `GET /project/{ProjectId}/task/{TaskId}/team//` (base URL `https://api.itmplatform.com/{{credentials.company}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-task-team.md) for the provider-specific parameters and requirements.


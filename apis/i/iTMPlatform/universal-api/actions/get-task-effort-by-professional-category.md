# ITM Platform: Get Task Effort by Professional Category



```
GET https://connect.mindcloud.co/v1/universal/iTMPlatform/latest/actions/get-task-effort-by-professional-category
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ITM Platform `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/iTMPlatform/latest/actions/get-task-effort-by-professional-category?connectionId=$CONNECTION_ID&projectId=string&taskId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "string",
  "taskId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/iTMPlatform/latest/actions/get-task-effort-by-professional-category?${params}`, {
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
      "category": {},
      "efforts": {},
      "isAutomaticActualEffortAccepted": true,
      "isDelete": true,
      "isOverload": true,
      "overloadDate": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `category` | object |  |
| `efforts` | object |  |
| `isAutomaticActualEffortAccepted` | boolean |  |
| `isDelete` | boolean |  |
| `isOverload` | boolean |  |
| `overloadDate` | string |  |

## Native endpoint

Through the native ITM Platform API, this operation is `GET /project/{ProjectId}/task/{TaskId}/effortbyprofessionalcategory` (base URL `https://api.itmplatform.com/{{credentials.company}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-task-effort-by-professional-category.md) for the provider-specific parameters and requirements.


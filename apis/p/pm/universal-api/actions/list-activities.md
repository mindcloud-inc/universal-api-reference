# 5pm: List Activities

Retrieves activities from 5pm.

```
GET https://connect.mindcloud.co/v1/universal/pm/latest/actions/list-activities
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 5pm `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pm/latest/actions/list-activities?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pm/latest/actions/list-activities?${params}`, {
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
      "count": 1,
      "items": [
        {
          "date": "2026-05-07T12:00:00.000Z",
          "id": "string",
          "projectId": 1,
          "taskId": 1,
          "text": "string",
          "type": "string"
        }
      ],
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number | Number of activities in this page. |
| `items[].date` | date | Activity posting date. |
| `items[].id` | string | Activity identifier. |
| `items[].projectId` | number | Related project ID. |
| `items[].taskId` | number | Related task ID. |
| `items[].text` | string | Activity text. |
| `items[].type` | string | Activity type. |
| `total` | number | Total number of activities available. |

## Native endpoint

Through the native 5pm API, this operation is `GET /service/get/activity/getList` (base URL `{{credentials.workspaceUrl}}/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-activities.md) for the provider-specific parameters and requirements.


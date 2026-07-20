# 5pm: List Files

Retrieves activity files from 5pm.

```
GET https://connect.mindcloud.co/v1/universal/pm/latest/actions/list-files
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 5pm `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pm/latest/actions/list-files?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pm/latest/actions/list-files?${params}`, {
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
          "activityId": 1,
          "id": "string",
          "name": "Ava Chen",
          "size": 1,
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
| `count` | number | Number of files in this page. |
| `items[].activityId` | number | Related activity ID. |
| `items[].id` | string | File identifier. |
| `items[].name` | string | File name. |
| `items[].size` | number | File size. |
| `items[].type` | string | File type. |
| `total` | number | Total number of files available. |

## Native endpoint

Through the native 5pm API, this operation is `GET /service/get/activity/getFilesList` (base URL `{{credentials.workspaceUrl}}/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-files.md) for the provider-specific parameters and requirements.


# PiAPI/Trellis: List Task History

Retrieves your task history from PiAPI/Trellis.

```
GET https://connect.mindcloud.co/v1/universal/piAPITrellis/latest/actions/list-task-history
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PiAPI/Trellis `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/piAPITrellis/latest/actions/list-task-history?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/piAPITrellis/latest/actions/list-task-history?${params}`, {
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
| `page` | number | no | History page number. Example: `1`. |
| `pageSize` | number | no | Number of history rows to return. Example: `10`. |
| `startTime` | number | no | Unix timestamp lower bound. Example: `1711929600`. |
| `endTime` | number | no | Unix timestamp upper bound. Example: `1712016000`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {}
      ],
      "page": 1,
      "size": 1,
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> |  |
| `page` | number |  |
| `size` | number |  |
| `total` | number |  |

## Native endpoint

Through the native PiAPI/Trellis API, this operation is `GET /api/open/tasks/histories` (base URL `https://api.piapi.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-task-history.md) for the provider-specific parameters and requirements.


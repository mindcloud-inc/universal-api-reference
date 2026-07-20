# PiAPI/Luma (unofficial): List PiAPI Luma Task History

Retrieves Luma task history from PiAPI.

```
GET https://connect.mindcloud.co/v1/universal/piAPILumaUnofficial/latest/actions/list-piapi-luma-task-history
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PiAPI/Luma (unofficial) `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/piAPILumaUnofficial/latest/actions/list-piapi-luma-task-history?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/piAPILumaUnofficial/latest/actions/list-piapi-luma-task-history?${params}`, {
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
| `startTime` | number | no | Optional Unix timestamp lower bound for task-history results. |
| `endTime` | number | no | Optional Unix timestamp upper bound for task-history results. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": 1,
      "data": {
        "data": [
          {}
        ],
        "page": 1,
        "size": 1,
        "total": 1
      },
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | number |  |
| `data` | object |  |
| `data.data` | array<object> |  |
| `data.page` | number |  |
| `data.size` | number |  |
| `data.total` | number |  |
| `message` | string |  |

## Native endpoint

Through the native PiAPI/Luma (unofficial) API, this operation is `GET /api/open/tasks/histories` (base URL `https://api.piapi.ai`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-piapi-luma-task-history.md) for the provider-specific parameters and requirements.


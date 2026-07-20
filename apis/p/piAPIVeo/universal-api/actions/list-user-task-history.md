# PiAPI/Veo: List User Task History

Retrieves user task history from PiAPI/Veo.

```
GET https://connect.mindcloud.co/v1/universal/piAPIVeo/latest/actions/list-user-task-history
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PiAPI/Veo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/piAPIVeo/latest/actions/list-user-task-history?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/piAPIVeo/latest/actions/list-user-task-history?${params}`, {
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
| `page` | number | no |  |
| `pageSize` | number | no |  |
| `model` | string | no |  |
| `startTime` | number | no |  |
| `endTime` | number | no |  |

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

Through the native PiAPI/Veo API, this operation is `GET /api/open/tasks/histories` (base URL `https://api.piapi.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-user-task-history.md) for the provider-specific parameters and requirements.


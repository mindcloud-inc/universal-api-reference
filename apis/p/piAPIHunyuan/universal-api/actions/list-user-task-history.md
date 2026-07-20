# PiAPI/Hunyuan: List User Task History



```
GET https://connect.mindcloud.co/v1/universal/piAPIHunyuan/latest/actions/list-user-task-history
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PiAPI/Hunyuan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/piAPIHunyuan/latest/actions/list-user-task-history?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/piAPIHunyuan/latest/actions/list-user-task-history?${params}`, {
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
| `data` | array<object> | Task history entries |
| `page` | number |  |
| `size` | number |  |
| `total` | number |  |

## Native endpoint

Through the native PiAPI/Hunyuan API, this operation is `GET /api/open/tasks/histories` (base URL `https://api.piapi.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-user-task-history.md) for the provider-specific parameters and requirements.


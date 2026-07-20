# PiAPI/FaceSwap: List User Task History

Retrieves user task history from PiAPI/FaceSwap.

```
GET https://connect.mindcloud.co/v1/universal/piAPIFaceSwap/latest/actions/list-user-task-history
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PiAPI/FaceSwap `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/piAPIFaceSwap/latest/actions/list-user-task-history?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/piAPIFaceSwap/latest/actions/list-user-task-history?${params}`, {
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
| `page` | number | no | History page number, starting from 1. Default: `1`. |
| `pageSize` | number | no | Number of history records per page, max 100. Default: `10`. |
| `model` | string | no | Optional PiAPI model filter such as image_toolkit or video_toolkit. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `startTime` | number | no | Unix timestamp in seconds for the earliest history entry to include. |
| `endTime` | number | no | Unix timestamp in seconds for the latest history entry to include. |

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
| `code` | number | PiAPI response code. |
| `data` | object | Paginated task history envelope. |
| `data.data` | array<object> | Task history rows for the requested page. |
| `data.page` | number | Current result page. |
| `data.size` | number | Number of results returned in this page. |
| `data.total` | number | Total matching task history records. |
| `message` | string | PiAPI response message. |

## Native endpoint

Through the native PiAPI/FaceSwap API, this operation is `GET /api/open/tasks/histories` (base URL `https://api.piapi.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-user-task-history.md) for the provider-specific parameters and requirements.


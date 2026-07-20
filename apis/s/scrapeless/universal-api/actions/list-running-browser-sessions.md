# Scrapeless: List Running Browser Sessions

Retrieves running browser sessions from Scrapeless.

```
GET https://connect.mindcloud.co/v1/universal/scrapeless/latest/actions/list-running-browser-sessions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Scrapeless `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scrapeless/latest/actions/list-running-browser-sessions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scrapeless/latest/actions/list-running-browser-sessions?${params}`, {
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
      "code": 1,
      "data": {
        "createTime": "string",
        "expireTime": "string",
        "metadata": {
          "session_name": "Ava Chen"
        },
        "state": "string",
        "success": true,
        "taskId": "string"
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
| `code` | number | code |
| `data` | array<object> | data |
| `data.createTime` | string | session create time |
| `data.expireTime` | string | session expire time |
| `data.metadata` | object | session metadata |
| `data.metadata.session_name` | string | session name |
| `data.state` | string | session state |
| `data.success` | boolean | task creation result |
| `data.taskId` | string | task id |
| `message` | string | message |

## Native endpoint

Through the native Scrapeless API, this operation is `GET /browser/running` (base URL `https://api.scrapeless.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-running-browser-sessions.md) for the provider-specific parameters and requirements.


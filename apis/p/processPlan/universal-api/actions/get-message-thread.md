# Process Plan: Get Message Thread



```
GET https://connect.mindcloud.co/v1/universal/processPlan/latest/actions/get-message-thread
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Process Plan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/processPlan/latest/actions/get-message-thread?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/processPlan/latest/actions/get-message-thread?${params}`, {
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
| `messageThreadId` | string | no | Message thread ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "developer_message": "string",
      "http_status_code": 1,
      "message_number": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `developer_message` | string |  |
| `http_status_code` | number |  |
| `message_number` | number |  |

## Native endpoint

Through the native Process Plan API, this operation is `GET /message_thread/:messageThreadId` (base URL `https://apius0.processplan.com/api/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-message-thread.md) for the provider-specific parameters and requirements.


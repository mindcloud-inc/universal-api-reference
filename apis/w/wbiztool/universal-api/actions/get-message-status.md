# Wbiztool: Get Message Status

Retrieves WhatsApp message delivery status from Wbiztool.

```
GET https://connect.mindcloud.co/v1/universal/wbiztool/latest/actions/get-message-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Wbiztool `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wbiztool/latest/actions/get-message-status?connectionId=$CONNECTION_ID&messageId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "messageId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/wbiztool/latest/actions/get-message-status?${params}`, {
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
| `messageId` | number | yes | Message ID to check in the URL path. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "error": "string",
      "message": "string",
      "status": 1,
      "statusText": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `error` | string |  |
| `message` | string |  |
| `status` | number |  |
| `statusText` | string |  |

## Native endpoint

Through the native Wbiztool API, this operation is `POST /message/status/{{message_id}}/` (base URL `https://wbiztool.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-message-status.md) for the provider-specific parameters and requirements.


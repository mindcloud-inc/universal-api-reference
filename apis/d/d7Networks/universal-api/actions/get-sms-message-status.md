# D7 Networks: Get SMS Message Status

Retrieves SMS delivery status from D7 Networks.

```
GET https://connect.mindcloud.co/v1/universal/d7Networks/latest/actions/get-sms-message-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a D7 Networks `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/d7Networks/latest/actions/get-sms-message-status?connectionId=$CONNECTION_ID&requestId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "requestId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/d7Networks/latest/actions/get-sms-message-status?${params}`, {
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
| `requestId` | string | yes | Request ID returned by the Send SMS action. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "channel": "string",
      "recipients": [
        {}
      ],
      "request_id": "string",
      "request_stage": "string",
      "total_recipients": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `channel` | string |  |
| `recipients` | array<object> |  |
| `request_id` | string |  |
| `request_stage` | string |  |
| `total_recipients` | number |  |

## Native endpoint

Through the native D7 Networks API, this operation is `GET /report/v1/message-log/:requestId` (base URL `https://api.d7networks.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-sms-message-status.md) for the provider-specific parameters and requirements.


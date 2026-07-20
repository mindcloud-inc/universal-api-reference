# ExpertTexting: Check Message Status

Retrieves message status from ExpertTexting by message ID.

```
GET https://connect.mindcloud.co/v1/universal/expertTexting/latest/actions/check-message-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ExpertTexting `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/expertTexting/latest/actions/check-message-status?connectionId=$CONNECTION_ID&messageId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "messageId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/expertTexting/latest/actions/check-message-status?${params}`, {
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
| `messageId` | string | yes | ExpertTexting message ID to check. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "deliveryStatus": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `deliveryStatus` | string | Delivery status returned by ExpertTexting for the target message ID. |

## Native endpoint

Through the native ExpertTexting API, this operation is `GET /ExptRestApi/sms/json/Message/Status` (base URL `https://www.experttexting.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/check-message-status.md) for the provider-specific parameters and requirements.


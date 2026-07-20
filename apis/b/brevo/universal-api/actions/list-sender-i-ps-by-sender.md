# Brevo: List Sender IPs by Sender



```
GET https://connect.mindcloud.co/v1/universal/brevo/latest/actions/list-sender-i-ps-by-sender
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Brevo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/brevo/latest/actions/list-sender-i-ps-by-sender?connectionId=$CONNECTION_ID&senderId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "senderId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/brevo/latest/actions/list-sender-i-ps-by-sender?${params}`, {
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
| `senderId` | number | yes | The sender identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "items": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `items` | array<object> |  |

## Native endpoint

Through the native Brevo API, this operation is `GET /v3/senders/:senderId/ips` (base URL `https://api.brevo.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-sender-i-ps-by-sender.md) for the provider-specific parameters and requirements.


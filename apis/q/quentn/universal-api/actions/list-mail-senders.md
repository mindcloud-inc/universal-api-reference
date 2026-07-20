# Quentn: List Mail Senders



```
GET https://connect.mindcloud.co/v1/universal/quentn/latest/actions/list-mail-senders
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Quentn `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/quentn/latest/actions/list-mail-senders?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/quentn/latest/actions/list-mail-senders?${params}`, {
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
      "mailSenders": [
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
| `mailSenders` | array<object> |  |

## Native endpoint

Through the native Quentn API, this operation is `GET /mail/senders` (base URL `https://tbg6y3.us-1.quentn.com/public/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-mail-senders.md) for the provider-specific parameters and requirements.


# Sensibot.io: Customer List

Retrieves customer lists from Sensibot.io.

```
GET https://connect.mindcloud.co/v1/universal/sensibotio/latest/actions/customer-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sensibot.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sensibotio/latest/actions/customer-list?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sensibotio/latest/actions/customer-list?${params}`, {
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
      "list": [
        [
          {}
        ]
      ],
      "status": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `list[]` | array<object> |  |
| `status` | number |  |

## Native endpoint

Through the native Sensibot.io API, this operation is `GET /whatsappcloud/customerlist` (base URL `https://api.sensibot.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/customer-list.md) for the provider-specific parameters and requirements.


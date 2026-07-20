# Usedesk: List Clients

Retrieves a list of clients from Usedesk.

```
GET https://connect.mindcloud.co/v1/universal/usedesk/latest/actions/list-clients
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Usedesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/usedesk/latest/actions/list-clients?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/usedesk/latest/actions/list-clients?${params}`, {
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
      "emails": [
        "ava@example.com"
      ],
      "id": 1,
      "name": "Ava Chen",
      "phone": "string",
      "tickets": [
        1
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `emails` | array<string> |  |
| `id` | number |  |
| `name` | string |  |
| `phone` | string |  |
| `tickets` | array<number> |  |

## Native endpoint

Through the native Usedesk API, this operation is `POST /clients` (base URL `https://secure.usedesk.com/uapi`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-clients.md) for the provider-specific parameters and requirements.


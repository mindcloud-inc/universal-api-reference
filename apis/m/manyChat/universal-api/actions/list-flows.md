# ManyChat: List Flows

Retrieves page flows from ManyChat.

```
GET https://connect.mindcloud.co/v1/universal/manyChat/latest/actions/list-flows
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ManyChat `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/manyChat/latest/actions/list-flows?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/manyChat/latest/actions/list-flows?${params}`, {
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
      "flows": [
        {
          "folderId": 1,
          "name": "Ava Chen",
          "ns": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `flows[].folderId` | number |  |
| `flows[].name` | string |  |
| `flows[].ns` | string |  |

## Native endpoint

Through the native ManyChat API, this operation is `GET /fb/page/getFlows` (base URL `https://api.manychat.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-flows.md) for the provider-specific parameters and requirements.


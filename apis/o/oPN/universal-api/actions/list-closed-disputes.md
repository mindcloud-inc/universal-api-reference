# OPN: List Closed Disputes

Retrieves a list of closed Disputes from OPN.

```
GET https://connect.mindcloud.co/v1/universal/oPN/latest/actions/list-closed-disputes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OPN `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/oPN/latest/actions/list-closed-disputes?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/oPN/latest/actions/list-closed-disputes?${params}`, {
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
      "data": [
        {}
      ],
      "from": "string",
      "limit": 1,
      "location": "string",
      "object": "string",
      "offset": 1,
      "order": "string",
      "to": "string",
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> |  |
| `from` | string |  |
| `limit` | number |  |
| `location` | string |  |
| `object` | string |  |
| `offset` | number |  |
| `order` | string |  |
| `to` | string |  |
| `total` | number |  |

## Native endpoint

Through the native OPN API, this operation is `GET /disputes/closed` (base URL `https://api.omise.co`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-closed-disputes.md) for the provider-specific parameters and requirements.


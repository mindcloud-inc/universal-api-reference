# IgnitePost: List Inserts

Retrieves available gift card inserts from IgnitePost.

```
GET https://connect.mindcloud.co/v1/universal/ignitePost/latest/actions/list-inserts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a IgnitePost `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ignitePost/latest/actions/list-inserts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ignitePost/latest/actions/list-inserts?${params}`, {
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
      "denomination": 1,
      "key": "string",
      "name": "Ava Chen",
      "purchaseFee": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `denomination` | number | Gift card or insert face value. |
| `key` | string | IgnitePOST insert key used when creating an order. |
| `name` | string | Display name of the insert option. |
| `purchaseFee` | number | Additional purchase fee charged for the insert. |

## Native endpoint

Through the native IgnitePost API, this operation is `GET /inserts` (base URL `https://dashboard.ignitepost.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-inserts.md) for the provider-specific parameters and requirements.


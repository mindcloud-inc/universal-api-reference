# PubNub: List Keysets

Retrieves keysets from PubNub.

```
GET https://connect.mindcloud.co/v1/universal/pubNub/latest/actions/list-keysets
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PubNub `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pubNub/latest/actions/list-keysets?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pubNub/latest/actions/list-keysets?${params}`, {
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
      "keysets": [
        {}
      ],
      "limit": 1,
      "page": 1,
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `keysets` | array<object> | The keysets returned in the current page. |
| `limit` | number | Page size. |
| `page` | number | Current page number. |
| `total` | number | Total number of keysets. |

## Native endpoint

Through the native PubNub API, this operation is `GET /keysets` (base URL `https://admin-api.pubnub.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-keysets.md) for the provider-specific parameters and requirements.


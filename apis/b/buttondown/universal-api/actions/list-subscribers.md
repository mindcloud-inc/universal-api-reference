# Buttondown: List Subscribers

Retrieves subscribers from Buttondown.

```
GET https://connect.mindcloud.co/v1/universal/buttondown/latest/actions/list-subscribers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Buttondown `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/buttondown/latest/actions/list-subscribers?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/buttondown/latest/actions/list-subscribers?${params}`, {
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
      "count": 1,
      "next": "string",
      "previous": "string",
      "results": [
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
| `count` | number | Total number of resources returned in this response window. |
| `next` | string | Pagination cursor or URL for the next page when Buttondown provides one. |
| `previous` | string | Pagination cursor or URL for the previous page when Buttondown provides one. |
| `results` | array<object> | The subscribers returned by Buttondown for the current connection. |

## Native endpoint

Through the native Buttondown API, this operation is `GET /subscribers` (base URL `https://api.buttondown.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-subscribers.md) for the provider-specific parameters and requirements.


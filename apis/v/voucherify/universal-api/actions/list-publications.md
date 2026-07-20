# Voucherify: List Publications

Retrieves a list of publications from Voucherify.

```
GET https://connect.mindcloud.co/v1/universal/voucherify/latest/actions/list-publications
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Voucherify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/voucherify/latest/actions/list-publications?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/voucherify/latest/actions/list-publications?${params}`, {
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
      "dataRef": "string",
      "object": "string",
      "publications": [
        {}
      ],
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `dataRef` | string |  |
| `object` | string |  |
| `publications` | array<object> |  |
| `total` | number |  |

## Native endpoint

Through the native Voucherify API, this operation is `GET /publications` (base URL `https://us1.api.voucherify.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-publications.md) for the provider-specific parameters and requirements.


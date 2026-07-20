# Voucherify: List Redemptions

Retrieves a list of redemptions from Voucherify.

```
GET https://connect.mindcloud.co/v1/universal/voucherify/latest/actions/list-redemptions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Voucherify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/voucherify/latest/actions/list-redemptions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/voucherify/latest/actions/list-redemptions?${params}`, {
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
      "redemptions": [
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
| `redemptions` | array<object> |  |
| `total` | number |  |

## Native endpoint

Through the native Voucherify API, this operation is `GET /redemptions` (base URL `https://us1.api.voucherify.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-redemptions.md) for the provider-specific parameters and requirements.


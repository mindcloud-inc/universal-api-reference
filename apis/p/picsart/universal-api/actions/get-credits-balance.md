# Picsart: Get Credits Balance

Retrieves your remaining Picsart credits balance.

```
GET https://connect.mindcloud.co/v1/universal/picsart/latest/actions/get-credits-balance
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Picsart `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/picsart/latest/actions/get-credits-balance?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/picsart/latest/actions/get-credits-balance?${params}`, {
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
      "credits": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `credits` | number | Remaining Picsart API credits. |

## Native endpoint

Through the native Picsart API, this operation is `GET /tools/1.0/balance` (base URL `https://api.picsart.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-credits-balance.md) for the provider-specific parameters and requirements.


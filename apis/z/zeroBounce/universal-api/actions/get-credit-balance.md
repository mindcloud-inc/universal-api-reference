# ZeroBounce: Get Credit Balance

Retrieves credit balance details from ZeroBounce.

```
GET https://connect.mindcloud.co/v1/universal/zeroBounce/latest/actions/get-credit-balance
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ZeroBounce `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zeroBounce/latest/actions/get-credit-balance?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zeroBounce/latest/actions/get-credit-balance?${params}`, {
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
      "credits": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `credits` | string | Remaining ZeroBounce credits. |

## Native endpoint

Through the native ZeroBounce API, this operation is `GET /v2/getcredits` (base URL `https://api.zerobounce.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-credit-balance.md) for the provider-specific parameters and requirements.


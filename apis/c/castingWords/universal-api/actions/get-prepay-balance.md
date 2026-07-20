# CastingWords: Get Prepay Balance

Retrieves prepay balance from CastingWords.

```
GET https://connect.mindcloud.co/v1/universal/castingWords/latest/actions/get-prepay-balance
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CastingWords `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/castingWords/latest/actions/get-prepay-balance?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/castingWords/latest/actions/get-prepay-balance?${params}`, {
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
      "balance": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `balance` | string | Current prepay balance in USD. |

## Native endpoint

Through the native CastingWords API, this operation is `GET prepay_balance` (base URL `https://castingwords.com/store/API4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-prepay-balance.md) for the provider-specific parameters and requirements.


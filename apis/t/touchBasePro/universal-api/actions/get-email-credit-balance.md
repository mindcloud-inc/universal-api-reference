# TouchBasePro: Get Email Credit Balance

Retrieves email credit balance from TouchBasePro.

```
GET https://connect.mindcloud.co/v1/universal/touchBasePro/latest/actions/get-email-credit-balance
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TouchBasePro `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/touchBasePro/latest/actions/get-email-credit-balance?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/touchBasePro/latest/actions/get-email-credit-balance?${params}`, {
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
      "creditCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `creditCount` | number |  |

## Native endpoint

Through the native TouchBasePro API, this operation is `GET /email/balance` (base URL `https://api.touchbasepro.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-email-credit-balance.md) for the provider-specific parameters and requirements.


# BetterContact: Check Credit Balance

Retrieves the current BetterContact credit balance and account email.

```
GET https://connect.mindcloud.co/v1/universal/betterContact/latest/actions/check-credit-balance
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BetterContact `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/betterContact/latest/actions/check-credit-balance?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/betterContact/latest/actions/check-credit-balance?${params}`, {
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
      "creditsLeft": "string",
      "email": "ava@example.com",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `creditsLeft` | string |  |
| `email` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native BetterContact API, this operation is `GET /account` (base URL `https://app.bettercontact.rocks/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/check-credit-balance.md) for the provider-specific parameters and requirements.


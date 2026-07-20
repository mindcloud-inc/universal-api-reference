# MessageBird: Get Balance



```
GET https://connect.mindcloud.co/v1/universal/messageBird/latest/actions/get-balance
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MessageBird `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/messageBird/latest/actions/get-balance?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/messageBird/latest/actions/get-balance?${params}`, {
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
      "amount": 1,
      "payment": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | number | Remaining balance amount. |
| `payment` | string | Balance payment type. |
| `type` | string | Balance record type. |

## Native endpoint

Through the native MessageBird API, this operation is `GET /balance` (base URL `https://api.bird.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-balance.md) for the provider-specific parameters and requirements.


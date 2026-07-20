# Proofy: Get Available Credits



```
GET https://connect.mindcloud.co/v1/universal/proofy/latest/actions/get-available-credits
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Proofy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/proofy/latest/actions/get-available-credits?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/proofy/latest/actions/get-available-credits?${params}`, {
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
| `credits` | number | Available Proofy credits remaining on the account. |

## Native endpoint

Through the native Proofy API, this operation is `GET /credits` (base URL `https://apis.proofy.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-available-credits.md) for the provider-specific parameters and requirements.


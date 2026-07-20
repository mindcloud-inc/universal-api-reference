# SMMCode: Get User Balance



```
GET https://connect.mindcloud.co/v1/universal/sMMCode/latest/actions/get-user-balance
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SMMCode `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sMMCode/latest/actions/get-user-balance?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sMMCode/latest/actions/get-user-balance?${params}`, {
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
      "balance": "string",
      "currency": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `balance` | string | Current account balance. |
| `currency` | string | Balance currency. |

## Native endpoint

Through the native SMMCode API, this operation is `POST /api/v2` (base URL `https://extended.smmcode.org`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user-balance.md) for the provider-specific parameters and requirements.


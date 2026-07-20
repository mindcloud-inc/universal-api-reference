# Splitwise: List Supported Currencies

Retrieves supported currencies from Splitwise.

```
GET https://connect.mindcloud.co/v1/universal/splitwise/latest/actions/list-supported-currencies
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Splitwise `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/splitwise/latest/actions/list-supported-currencies?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/splitwise/latest/actions/list-supported-currencies?${params}`, {
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
      "currencies": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `currencies` | array<object> | Supported currencies returned by Splitwise. |

## Native endpoint

Through the native Splitwise API, this operation is `GET /get_currencies` (base URL `https://secure.splitwise.com/api/v3.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-supported-currencies.md) for the provider-specific parameters and requirements.


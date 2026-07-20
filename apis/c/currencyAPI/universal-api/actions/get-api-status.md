# CurrencyAPI: Get API Status

Retrieves current API quota status from CurrencyAPI.

```
GET https://connect.mindcloud.co/v1/universal/currencyAPI/latest/actions/get-api-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CurrencyAPI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/currencyAPI/latest/actions/get-api-status?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/currencyAPI/latest/actions/get-api-status?${params}`, {
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
      "accountId": 1,
      "quotas": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountId` | number | CurrencyAPI account identifier |
| `quotas` | object | Quota usage grouped by period |

## Native endpoint

Through the native CurrencyAPI API, this operation is `GET /v3/status` (base URL `https://api.currencyapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-api-status.md) for the provider-specific parameters and requirements.


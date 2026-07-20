# CoinGate: List Billing Requests

Retrieves billing requests from your CoinGate account.

```
GET https://connect.mindcloud.co/v1/universal/coinGate/latest/actions/list-billing-requests
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CoinGate `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/coinGate/latest/actions/list-billing-requests?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/coinGate/latest/actions/list-billing-requests?${params}`, {
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
      "billingRequests": [
        {
          "id": 1
        }
      ],
      "currentPage": 1,
      "perPage": 1,
      "totalPages": 1,
      "totalRecords": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `billingRequests[].id` | number |  |
| `currentPage` | number |  |
| `perPage` | number |  |
| `totalPages` | number |  |
| `totalRecords` | number |  |

## Native endpoint

Through the native CoinGate API, this operation is `GET /billing/requests` (base URL `https://api.coingate.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-billing-requests.md) for the provider-specific parameters and requirements.


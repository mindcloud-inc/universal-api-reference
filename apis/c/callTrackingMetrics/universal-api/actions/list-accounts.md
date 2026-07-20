# CallTrackingMetrics: List Accounts

Retrieves all available accounts from CallTrackingMetrics.

```
GET https://connect.mindcloud.co/v1/universal/callTrackingMetrics/latest/actions/list-accounts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CallTrackingMetrics `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/callTrackingMetrics/latest/actions/list-accounts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/callTrackingMetrics/latest/actions/list-accounts?${params}`, {
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
      "accounts": [
        [
          {}
        ]
      ],
      "nextPage": 1,
      "page": 1,
      "perPage": 1,
      "previousPage": 1,
      "totalEntries": 1,
      "totalPages": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accounts[]` | array<object> |  |
| `accounts[].agencyId` | number |  |
| `accounts[].created` | date |  |
| `accounts[].id` | number |  |
| `accounts[].name` | string |  |
| `accounts[].status` | string |  |
| `accounts[].updated` | date |  |
| `accounts[].url` | string |  |
| `accounts[].userRole` | string |  |
| `nextPage` | number |  |
| `page` | number |  |
| `perPage` | number |  |
| `previousPage` | number |  |
| `totalEntries` | number |  |
| `totalPages` | number |  |

## Native endpoint

Through the native CallTrackingMetrics API, this operation is `GET /accounts.json` (base URL `https://api.calltrackingmetrics.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-accounts.md) for the provider-specific parameters and requirements.


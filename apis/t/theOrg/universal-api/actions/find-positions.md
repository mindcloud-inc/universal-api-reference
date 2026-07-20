# The Org: Find Positions

Finds positions in The Org by search filters.

```
GET https://connect.mindcloud.co/v1/universal/theOrg/latest/actions/find-positions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a The Org `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/theOrg/latest/actions/find-positions?connectionId=$CONNECTION_ID&limit=1&offset=0&filters=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "limit": "1",
  "offset": "0",
  "filters": "[object Object]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/theOrg/latest/actions/find-positions?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `limit` | number | yes | Maximum number of results to return, up to 1000. Default: `1`. |
| `offset` | number | yes | Result offset, up to 10000. Default: `0`. |
| `filters` | object | yes | Search filters object matching the official Position API contract. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "items": [
          {}
        ],
        "totalCreditsUsed": 1,
        "totalResults": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.items` | array<object> | Matching positions returned by The Org |
| `data.totalCreditsUsed` | number | Credits charged for the returned rows |
| `data.totalResults` | number | Total matches for the search filters |

## Native endpoint

Through the native The Org API, this operation is `POST /v1.1/positions` (base URL `https://api.theorg.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/find-positions.md) for the provider-specific parameters and requirements.


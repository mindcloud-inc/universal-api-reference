# The Org: Estimate Position Search Credit Usage

Estimates position search credit usage in The Org.

```
GET https://connect.mindcloud.co/v1/universal/theOrg/latest/actions/estimate-position-search-credit-usage
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a The Org `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/theOrg/latest/actions/estimate-position-search-credit-usage?connectionId=$CONNECTION_ID&limit=1&offset=0&filters=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "limit": "1",
  "offset": "0",
  "filters": "[object Object]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/theOrg/latest/actions/estimate-position-search-credit-usage?${params}`, {
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
        "creditCost": 1,
        "remainingCredits": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.creditCost` | number | Estimated credits required for the supplied position search |
| `data.remainingCredits` | number | Remaining credits after applying the estimate |

## Native endpoint

Through the native The Org API, this operation is `POST /v1.1/positions/credit-usage` (base URL `https://api.theorg.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/estimate-position-search-credit-usage.md) for the provider-specific parameters and requirements.


# G2: Retrieve Market Signals

Retrieves category buyer intent signals from G2 for a date range.

```
GET https://connect.mindcloud.co/v1/universal/g2/latest/actions/retrieve-market-signals
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a G2 `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/g2/latest/actions/retrieve-market-signals?connectionId=$CONNECTION_ID&limit=25&offset=0&categoryIds=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "categoryIds": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/g2/latest/actions/retrieve-market-signals?${params}`, {
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
| `categoryIds` | string | yes | Category IDs to scope market signals. |
| `endDate` | date | no | End date for the market signals range. |
| `startDate` | date | no | Start date for the market signals range. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {
        "categoryUuid": "string",
        "companyDomain": "string",
        "companyName": "Ava Chen",
        "endDate": "string",
        "startDate": "string"
      },
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attributes.categoryUuid` | string |  |
| `attributes.companyDomain` | string |  |
| `attributes.companyName` | string |  |
| `attributes.endDate` | string |  |
| `attributes.startDate` | string |  |
| `type` | string |  |

## Native endpoint

Through the native G2 API, this operation is `GET /api/v2/market_signals` (base URL `https://data.g2.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/retrieve-market-signals.md) for the provider-specific parameters and requirements.


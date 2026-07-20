# Finnhub: List Stock Upgrades Downgrades

Retrieves stock upgrades and downgrades from Finnhub.

```
GET https://connect.mindcloud.co/v1/universal/finnhub/latest/actions/list-stock-upgrades-downgrades
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Finnhub `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/finnhub/latest/actions/list-stock-upgrades-downgrades?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/finnhub/latest/actions/list-stock-upgrades-downgrades?${params}`, {
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
| `symbol` | string | no | Optional company symbol. Leave blank for latest upgrades and downgrades. Example: `e.g. AAPL`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `from` | string | no | Start date in YYYY-MM-DD format. Example: `2025-01-01`. |
| `to` | string | no | End date in YYYY-MM-DD format. Example: `2025-12-31`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "action": "string",
      "company": "string",
      "fromGrade": "string",
      "gradeTime": 1,
      "symbol": "string",
      "toGrade": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `action` | string |  |
| `company` | string |  |
| `fromGrade` | string |  |
| `gradeTime` | number |  |
| `symbol` | string |  |
| `toGrade` | string |  |

## Native endpoint

Through the native Finnhub API, this operation is `GET /stock/upgrade-downgrade` (base URL `https://finnhub.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-stock-upgrades-downgrades.md) for the provider-specific parameters and requirements.


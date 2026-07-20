# MoySklad: Get money plot series report

Retrieves the money plot series report from MoySklad.

```
GET https://connect.mindcloud.co/v1/universal/moySklad/latest/actions/get-money-plot-series-report
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MoySklad `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/moySklad/latest/actions/get-money-plot-series-report?connectionId=$CONNECTION_ID&interval=day&momentFrom=2026-01-01%2000%3A00%3A00&momentTo=2026-12-31%2023%3A59%3A59" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "interval": "day",
  "momentFrom": "2026-01-01 00:00:00",
  "momentTo": "2026-12-31 23:59:59"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/moySklad/latest/actions/get-money-plot-series-report?${params}`, {
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
| `interval` | string | yes | MoySklad interval argument. Default: `day`. |
| `momentFrom` | string | yes | MoySklad momentFrom argument. Default: `2026-01-01 00:00:00`. |
| `momentTo` | string | yes | MoySklad momentTo argument. Default: `2026-12-31 23:59:59`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "context": {},
      "meta": {},
      "series": [
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
| `context` | object |  |
| `meta` | object |  |
| `series` | array<object> |  |

## Native endpoint

Through the native MoySklad API, this operation is `GET report/money/plotseries` (base URL `https://api.moysklad.ru/api/remap/1.2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-money-plot-series-report.md) for the provider-specific parameters and requirements.


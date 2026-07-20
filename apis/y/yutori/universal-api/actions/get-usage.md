# Yutori: Get Usage

Retrieves Yutori account usage, active scouts, and rate limits.

```
GET https://connect.mindcloud.co/v1/universal/yutori/latest/actions/get-usage
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Yutori `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/yutori/latest/actions/get-usage?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/yutori/latest/actions/get-usage?${params}`, {
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
| `period` | string | no | Usage window to return: 24h, 7d, 30d, or 90d. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active_scout_ids": [
        "string"
      ],
      "activity": {},
      "n1_rate_limits": {},
      "num_active_scouts": 1,
      "rate_limits": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active_scout_ids` | array |  |
| `activity` | object |  |
| `n1_rate_limits` | object |  |
| `num_active_scouts` | number |  |
| `rate_limits` | object |  |

## Native endpoint

Through the native Yutori API, this operation is `GET /v1/usage` (base URL `https://api.yutori.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-usage.md) for the provider-specific parameters and requirements.


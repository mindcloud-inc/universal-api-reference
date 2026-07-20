# Lunch Money: Get budget summary



```
GET https://connect.mindcloud.co/v1/universal/lunchMoney/latest/actions/get-budget-summary
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lunch Money `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lunchMoney/latest/actions/get-budget-summary?connectionId=$CONNECTION_ID&start_date=string&end_date=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "start_date": "string",
  "end_date": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lunchMoney/latest/actions/get-budget-summary?${params}`, {
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
| `start_date` | string | yes | Inclusive start date (YYYY-MM-DD). |
| `end_date` | string | yes | Inclusive end date (YYYY-MM-DD). |
| `include_totals` | boolean | no |  |
| `include_occurrences` | boolean | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "categoryId": 1,
      "occurrences": [
        {}
      ],
      "totals": {
        "otherActivity": 1,
        "recurringActivity": 1,
        "recurringExpected": 1,
        "recurringRemaining": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `categoryId` | number |  |
| `occurrences` | array<object> |  |
| `totals` | object |  |
| `totals.otherActivity` | number |  |
| `totals.recurringActivity` | number |  |
| `totals.recurringExpected` | number |  |
| `totals.recurringRemaining` | number |  |

## Native endpoint

Through the native Lunch Money API, this operation is `GET /summary` (base URL `https://api.lunchmoney.dev/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-budget-summary.md) for the provider-specific parameters and requirements.


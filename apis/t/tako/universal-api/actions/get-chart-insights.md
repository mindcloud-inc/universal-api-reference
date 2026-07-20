# Tako: Get Chart Insights

Retrieves insights from a Tako knowledge card chart.

```
GET https://connect.mindcloud.co/v1/universal/tako/latest/actions/get-chart-insights
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tako `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tako/latest/actions/get-chart-insights?connectionId=$CONNECTION_ID&cardId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "cardId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tako/latest/actions/get-chart-insights?${params}`, {
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
| `cardId` | string | yes | ID of the chart knowledge card to inspect. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "description": "string",
      "insights": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string | Natural-language description of the analyzed chart. |
| `insights` | array<string> | Insight strings extracted from the referenced chart. |

## Native endpoint

Through the native Tako API, this operation is `GET /v1/beta/chart_insights` (base URL `https://tako.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-chart-insights.md) for the provider-specific parameters and requirements.


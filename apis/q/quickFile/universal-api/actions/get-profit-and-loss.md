# QuickFile: Get Profit And Loss



```
GET https://connect.mindcloud.co/v1/universal/quickFile/latest/actions/get-profit-and-loss
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a QuickFile `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/quickFile/latest/actions/get-profit-and-loss?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/quickFile/latest/actions/get-profit-and-loss?${params}`, {
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
| `fromDate` | date | no | Start date for the profit and loss period. |
| `toDate` | date | no | End date for the profit and loss period. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "lessCostOfSales": 1,
      "lessExpenses": 1,
      "netProfit": 1,
      "turnover": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `lessCostOfSales` | number | Total cost of sales for the selected period. |
| `lessExpenses` | number | Total expenses for the selected period. |
| `netProfit` | number | Net profit for the selected period. |
| `turnover` | number | Total turnover for the selected period. |

## Native endpoint

Through the native QuickFile API, this operation is `POST /report/profitandloss` (base URL `https://api.quickfile.co.uk/1_2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-profit-and-loss.md) for the provider-specific parameters and requirements.


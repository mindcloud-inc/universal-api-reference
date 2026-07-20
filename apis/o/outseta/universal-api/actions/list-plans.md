# Outseta: List Plans

Retrieves a list of plans from Outseta.

```
GET https://connect.mindcloud.co/v1/universal/outseta/latest/actions/list-plans
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Outseta `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/outseta/latest/actions/list-plans?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/outseta/latest/actions/list-plans?${params}`, {
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
      "AnnualRate": 1,
      "Created": "string",
      "IsQuantityEditable": true,
      "IsTaxable": true,
      "MinimumQuantity": 1,
      "MonthlyRate": 1,
      "Name": "Ava Chen",
      "PlanAddOns": "string",
      "PlanFamily": "string",
      "SetupFee": 1,
      "TrialPeriodDays": 1,
      "Uid": "string",
      "UnitOfMeasure": "string",
      "Updated": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `AnnualRate` | number |  |
| `Created` | string |  |
| `IsQuantityEditable` | boolean |  |
| `IsTaxable` | boolean |  |
| `MinimumQuantity` | number |  |
| `MonthlyRate` | number |  |
| `Name` | string |  |
| `PlanAddOns` | string |  |
| `PlanFamily` | string |  |
| `SetupFee` | number |  |
| `TrialPeriodDays` | number |  |
| `Uid` | string |  |
| `UnitOfMeasure` | string |  |
| `Updated` | string |  |

## Native endpoint

Through the native Outseta API, this operation is `GET /billing/plans` (base URL `https://{{credentials.subdomain}}.outseta.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-plans.md) for the provider-specific parameters and requirements.


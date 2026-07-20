# LeadIQ: Get Account



```
GET https://connect.mindcloud.co/v1/universal/leadIQ/latest/actions/get-account
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LeadIQ `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/leadIQ/latest/actions/get-account?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/leadIQ/latest/actions/get-account?${params}`, {
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
      "dataHubPlan": {
        "available": 1,
        "name": "Ava Chen",
        "nextBillingPeriod": "2026-05-07T12:00:00.000Z",
        "product": "string",
        "status": "string",
        "used": 1
      },
      "plans": [
        {
          "name": "Ava Chen",
          "nextBillingPeriod": "2026-05-07T12:00:00.000Z",
          "product": "string",
          "status": "string"
        }
      ],
      "universalPlan": {
        "available": 1,
        "name": "Ava Chen",
        "nextBillingPeriod": "2026-05-07T12:00:00.000Z",
        "product": "string",
        "status": "string",
        "used": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `dataHubPlan.available` | number |  |
| `dataHubPlan.name` | string |  |
| `dataHubPlan.nextBillingPeriod` | date |  |
| `dataHubPlan.product` | string |  |
| `dataHubPlan.status` | string |  |
| `dataHubPlan.used` | number |  |
| `plans[].name` | string |  |
| `plans[].nextBillingPeriod` | date |  |
| `plans[].product` | string |  |
| `plans[].status` | string |  |
| `universalPlan.available` | number |  |
| `universalPlan.name` | string |  |
| `universalPlan.nextBillingPeriod` | date |  |
| `universalPlan.product` | string |  |
| `universalPlan.status` | string |  |
| `universalPlan.used` | number |  |

## Native endpoint

Through the native LeadIQ API, this operation is `POST graphql` (base URL `https://api.leadiq.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-account.md) for the provider-specific parameters and requirements.


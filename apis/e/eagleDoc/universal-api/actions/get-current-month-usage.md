# Eagle Doc: Get Current Month Usage

Retrieves current month usage from Eagle Doc.

```
GET https://connect.mindcloud.co/v1/universal/eagleDoc/latest/actions/get-current-month-usage
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Eagle Doc `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eagleDoc/latest/actions/get-current-month-usage?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eagleDoc/latest/actions/get-current-month-usage?${params}`, {
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
      "contractQuota": 1,
      "currentMonth": "string",
      "endedAt": "2026-05-07T12:00:00.000Z",
      "hardLimit": 1,
      "overUsage": 1,
      "overUsageAllowed": true,
      "overUsageCost": 1,
      "pricePerPageOverUsage": 1,
      "quotaUsed": 1,
      "startedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contractQuota` | number | Number of pages included in the contract quota |
| `currentMonth` | string | Current billing month in YYYY-MM format |
| `endedAt` | date | Billing period end time |
| `hardLimit` | number | Hard processing ceiling for the billing period |
| `overUsage` | number | Pages processed above the contract quota |
| `overUsageAllowed` | boolean | Whether processing above the contract quota is allowed |
| `overUsageCost` | number | Accumulated over-usage cost for the current billing period |
| `pricePerPageOverUsage` | number | Price charged per page above the contract quota |
| `quotaUsed` | number | Pages processed in the current billing period |
| `startedAt` | date | Billing period start time |

## Native endpoint

Through the native Eagle Doc API, this operation is `GET /api/usage/v1/current` (base URL `https://de.eagle-doc.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-current-month-usage.md) for the provider-specific parameters and requirements.


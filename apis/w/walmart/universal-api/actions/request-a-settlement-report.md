# Walmart: Request a settlement report

Use this report to review detailed itemization of Walmart Fulfillment Services (WFS) and Multichannel Solutions (MCS) fees and credits for a selected time period. It provides a transaction-level view of charges, adjustments, and credits to help reconcile final WFS settlements.

```
POST https://connect.mindcloud.co/v1/universal/walmart/latest/actions/request-a-settlement-report
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Walmart `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/walmart/latest/actions/request-a-settlement-report" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/walmart/latest/actions/request-a-settlement-report', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `dataStartTime` | string | no |  |
| `dataEndTime` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Walmart API returns.

## Native endpoint

Through the native Walmart API, this operation is `POST https://marketplace.walmartapis.com/v3/reports/reportRequests?reportType=SETTLEMENT&reportVersion=v1` (base URL `https://{{credentials.environment}}.walmartapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/request-a-settlement-report.md) for the provider-specific parameters and requirements.


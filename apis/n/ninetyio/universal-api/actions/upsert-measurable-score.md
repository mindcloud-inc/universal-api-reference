# Ninety.io: Create or Update Measurable Score

Creates or updates a measurable score in Ninety.io for a period.

```
PUT https://connect.mindcloud.co/v1/universal/ninetyio/latest/actions/upsert-measurable-score
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ninety.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/ninetyio/latest/actions/upsert-measurable-score" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "kpiId": "string",
  "value": 1,
  "periodStartDate": "2026-05-07T12:00:00.000Z"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ninetyio/latest/actions/upsert-measurable-score', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "kpiId": "string",
    "value": 1,
    "periodStartDate": "2026-05-07T12:00:00.000Z"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `kpiId` | string | yes |  |
| `value` | number | yes |  |
| `periodStartDate` | date | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Ninety.io API returns.

## Native endpoint

Through the native Ninety.io API, this operation is `POST /v1/scorecard/kpis/:kpiId/scores` (base URL `https://api.public.ninety.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upsert-measurable-score.md) for the provider-specific parameters and requirements.


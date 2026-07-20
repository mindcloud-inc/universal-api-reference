# CoachAccountable: Add Metric Data

Adds metric data in CoachAccountable.

```
POST https://connect.mindcloud.co/v1/universal/coachAccountable/latest/actions/add-metric-data
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CoachAccountable `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/coachAccountable/latest/actions/add-metric-data" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "metricId": 1,
  "dateOf": "2026-05-07T12:00:00.000Z",
  "value": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/coachAccountable/latest/actions/add-metric-data', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "metricId": 1,
    "dateOf": "2026-05-07T12:00:00.000Z",
    "value": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `metricId` | number | yes | ID of the Metric to which data is to be added. |
| `dateOf` | date | yes |  |
| `value` | number | yes |  |
| `comment` | string | no | Optional note about this data point. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native CoachAccountable API returns.

## Native endpoint

Through the native CoachAccountable API, this operation is `POST /` (base URL `https://www.coachaccountable.com/API`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-metric-data.md) for the provider-specific parameters and requirements.


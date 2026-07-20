# Linkila: Count Analytics By Interval

Retrieves Linkila analytics counts by time interval.

```
GET https://connect.mindcloud.co/v1/universal/linkila/latest/actions/count-analytics-by-interval
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Linkila `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/linkila/latest/actions/count-analytics-by-interval?connectionId=$CONNECTION_ID&granularity=string&startTimestamp=2026-05-07T12%3A00%3A00.000Z&endTimestamp=2026-05-07T12%3A00%3A00.000Z&timezoneName=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "granularity": "string",
  "startTimestamp": "2026-05-07T12:00:00.000Z",
  "endTimestamp": "2026-05-07T12:00:00.000Z",
  "timezoneName": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/linkila/latest/actions/count-analytics-by-interval?${params}`, {
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
| `granularity` | string | yes | Required interval granularity. Official values: day, hour, minute. |
| `startTimestamp` | date | yes | Required ISO date-time start timestamp for the analytics interval. |
| `endTimestamp` | date | yes | Required ISO date-time end timestamp for the analytics interval. |
| `timezoneName` | string | yes | Required IANA timezone name used to group interval counts. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `filter` | object | no | Optional Linkila analytics filter object. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> | Analytics interval rows with datetime and visits. |

## Native endpoint

Through the native Linkila API, this operation is `POST /analytics/countByInterval` (base URL `https://app.linkila.com/integrations/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/count-analytics-by-interval.md) for the provider-specific parameters and requirements.


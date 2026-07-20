# Routee: View Volume and Price Analytics for a range of Lookup Records

Retrieves volume and price analytics for a range of lookup records from Routee.

```
GET https://connect.mindcloud.co/v1/universal/routee/latest/actions/view-volume-and-price-analytics-for-a-range-of-lookup-records
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Routee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/routee/latest/actions/view-volume-and-price-analytics-for-a-range-of-lookup-records?connectionId=$CONNECTION_ID&startDate=2026-05-07T12%3A00%3A00.000Z&endDate=2026-05-07T12%3A00%3A00.000Z" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "startDate": "2026-05-07T12:00:00.000Z",
  "endDate": "2026-05-07T12:00:00.000Z"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/routee/latest/actions/view-volume-and-price-analytics-for-a-range-of-lookup-records?${params}`, {
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
| `startDate` | date | yes | starting date to get reports |
| `endDate` | date | yes | ending date to get reports |

## Response

```json
{
  "success": true,
  "data": [
    {
      "details": [
        [
          {}
        ]
      ],
      "totals": {
        "timeGrouping": "string",
        "totalAbsent": "string",
        "totalActive": "string",
        "totalCount": "string",
        "totalFailed": "string",
        "totalPrice": "string",
        "totalQueued": "string",
        "totalUnknown": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `details[]` | array<object> |  |
| `details[].absentCount` | string |  |
| `details[].activeCount` | string |  |
| `details[].count` | string |  |
| `details[].failedCount` | string |  |
| `details[].price` | string |  |
| `details[].queuedCount` | string |  |
| `details[].startDateTime` | string |  |
| `details[].unknownCount` | string |  |
| `totals` | object |  |
| `totals.timeGrouping` | string |  |
| `totals.totalAbsent` | string |  |
| `totals.totalActive` | string |  |
| `totals.totalCount` | string |  |
| `totals.totalFailed` | string |  |
| `totals.totalPrice` | string |  |
| `totals.totalQueued` | string |  |
| `totals.totalUnknown` | string |  |

## Native endpoint

Through the native Routee API, this operation is `GET /reports/my/lookup/volPrice` (base URL `https://connect.routee.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/view-volume-and-price-analytics-for-a-range-of-lookup-records.md) for the provider-specific parameters and requirements.


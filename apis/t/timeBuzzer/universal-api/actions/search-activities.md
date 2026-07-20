# timeBuzzer: Search Activities



```
GET https://connect.mindcloud.co/v1/universal/timeBuzzer/latest/actions/search-activities
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a timeBuzzer `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/timeBuzzer/latest/actions/search-activities?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/timeBuzzer/latest/actions/search-activities?${params}`, {
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
| `userIds[]` | array<number> | no | Optional user IDs to include. Accepts multiple values as an array. |
| `startDate` | string | no | The inclusive start timestamp in ISO 8601 format. |
| `endDate` | string | no | The inclusive end timestamp in ISO 8601 format. |
| `strictDate` | boolean | no | Whether the date boundaries should be strict. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "activities": [
        {}
      ],
      "totalCount": 1,
      "totalDuration": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `activities` | array<object> | Activity rows returned for the current filtered page. |
| `totalCount` | number | Total number of activities matching the current filtered query. |
| `totalDuration` | number | Total duration for the filtered activity result set. |

## Native endpoint

Through the native timeBuzzer API, this operation is `POST /open-api/activities/filters` (base URL `https://my.timebuzzer.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/search-activities.md) for the provider-specific parameters and requirements.


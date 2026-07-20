# Ventrata: Get Batch Availability Calendar

Retrieves batch availability calendar data from Ventrata.

```
GET https://connect.mindcloud.co/v1/universal/ventrata/latest/actions/get-batch-availability-calendar
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ventrata `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ventrata/latest/actions/get-batch-availability-calendar?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ventrata/latest/actions/get-batch-availability-calendar?${params}`, {
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
      "availabilityLocalStartTimes": [
        "string"
      ],
      "available": true,
      "limitPaxCount": 1,
      "localDate": "2026-05-07T12:00:00.000Z",
      "noShows": 1,
      "openingHours": [
        {
          "from": "string",
          "to": "string"
        }
      ],
      "optionId": "string",
      "paxCount": 1,
      "paxWeight": 1,
      "productId": "string",
      "status": "string",
      "statusCode": "string",
      "statusMessage": "string",
      "totalNoShows": 1,
      "totalPaxCount": 1,
      "totalPaxWeight": 1,
      "utcCutoffAt": "2026-05-07T12:00:00.000Z",
      "weightUnit": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `availabilityLocalStartTimes[]` | string |  |
| `available` | boolean |  |
| `limitPaxCount` | number |  |
| `localDate` | date |  |
| `noShows` | number |  |
| `openingHours[].from` | string |  |
| `openingHours[].to` | string |  |
| `optionId` | string |  |
| `paxCount` | number |  |
| `paxWeight` | number |  |
| `productId` | string |  |
| `status` | string |  |
| `statusCode` | string |  |
| `statusMessage` | string |  |
| `totalNoShows` | number |  |
| `totalPaxCount` | number |  |
| `totalPaxWeight` | number |  |
| `utcCutoffAt` | date |  |
| `weightUnit` | string |  |

## Native endpoint

Through the native Ventrata API, this operation is `POST octo/availability/calendar/batch` (base URL `https://api.ventrata.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-batch-availability-calendar.md) for the provider-specific parameters and requirements.


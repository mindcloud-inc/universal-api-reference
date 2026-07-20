# Ventrata: Get Batch Availability

Retrieves batch availability from Ventrata.

```
GET https://connect.mindcloud.co/v1/universal/ventrata/latest/actions/get-batch-availability
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ventrata `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ventrata/latest/actions/get-batch-availability?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ventrata/latest/actions/get-batch-availability?${params}`, {
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
      "allDay": true,
      "available": true,
      "id": "string",
      "limitPaxCount": 1,
      "localDateTimeEnd": "2026-05-07T12:00:00.000Z",
      "localDateTimeStart": "2026-05-07T12:00:00.000Z",
      "noShows": 1,
      "openingHours": [
        {
          "from": "string",
          "to": "string"
        }
      ],
      "optionId": "string",
      "paxCount": 1,
      "productId": "string",
      "status": "string",
      "statusCode": "string",
      "statusMessage": "string",
      "totalNoShows": 1,
      "totalPaxCount": 1,
      "utcCutoffAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `allDay` | boolean |  |
| `available` | boolean |  |
| `id` | string |  |
| `limitPaxCount` | number |  |
| `localDateTimeEnd` | date |  |
| `localDateTimeStart` | date |  |
| `noShows` | number |  |
| `openingHours[].from` | string |  |
| `openingHours[].to` | string |  |
| `optionId` | string |  |
| `paxCount` | number |  |
| `productId` | string |  |
| `status` | string |  |
| `statusCode` | string |  |
| `statusMessage` | string |  |
| `totalNoShows` | number |  |
| `totalPaxCount` | number |  |
| `utcCutoffAt` | date |  |

## Native endpoint

Through the native Ventrata API, this operation is `POST octo/availability/batch` (base URL `https://api.ventrata.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-batch-availability.md) for the provider-specific parameters and requirements.


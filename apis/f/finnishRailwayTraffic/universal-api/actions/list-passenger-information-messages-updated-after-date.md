# Finnish Railway Traffic: List passenger information messages updated after date

Retrieves passenger information messages updated after a date in Finnish Railway Traffic.

```
GET https://connect.mindcloud.co/v1/universal/finnishRailwayTraffic/latest/actions/list-passenger-information-messages-updated-after-date
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Finnish Railway Traffic `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/finnishRailwayTraffic/latest/actions/list-passenger-information-messages-updated-after-date?connectionId=$CONNECTION_ID&date=2026-05-07T12%3A00%3A00.000Z" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "date": "2026-05-07T12:00:00.000Z"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/finnishRailwayTraffic/latest/actions/list-passenger-information-messages-updated-after-date?${params}`, {
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
| `date` | date | yes | Departure date used by Digitraffic for the passenger information update lookup. Use ISO date format YYYY-MM-DD. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "audio": {},
      "id": "string",
      "stations": [
        "string"
      ],
      "trainDepartureDate": "2026-05-07T12:00:00.000Z",
      "trainNumber": 1,
      "version": 1,
      "video": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `audio` | object |  |
| `id` | string |  |
| `stations` | array<string> |  |
| `trainDepartureDate` | date |  |
| `trainNumber` | number |  |
| `version` | number |  |
| `video` | object |  |

## Native endpoint

Through the native Finnish Railway Traffic API, this operation is `GET /api/v1/passenger-information/updated-after/:date` (base URL `https://rata.digitraffic.fi`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-passenger-information-messages-updated-after-date.md) for the provider-specific parameters and requirements.


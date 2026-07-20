# Finnish Railway Traffic: List compositions by departure date

Retrieves train compositions by departure date from Finnish Railway Traffic.

```
GET https://connect.mindcloud.co/v1/universal/finnishRailwayTraffic/latest/actions/list-compositions-by-departure-date
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Finnish Railway Traffic `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/finnishRailwayTraffic/latest/actions/list-compositions-by-departure-date?connectionId=$CONNECTION_ID&departureDate=2026-05-07T12%3A00%3A00.000Z" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "departureDate": "2026-05-07T12:00:00.000Z"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/finnishRailwayTraffic/latest/actions/list-compositions-by-departure-date?${params}`, {
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
| `departureDate` | date | yes | Train departure date. Use ISO date format YYYY-MM-DD. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "departureDate": "2026-05-07T12:00:00.000Z",
      "journeySections": [
        {}
      ],
      "operatorShortCode": "string",
      "operatorUICCode": 1,
      "trainCategory": "string",
      "trainNumber": 1,
      "trainType": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `departureDate` | date |  |
| `journeySections` | array<object> |  |
| `operatorShortCode` | string |  |
| `operatorUICCode` | number |  |
| `trainCategory` | string |  |
| `trainNumber` | number |  |
| `trainType` | string |  |

## Native endpoint

Through the native Finnish Railway Traffic API, this operation is `GET /api/v1/compositions/:departure_date` (base URL `https://rata.digitraffic.fi`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-compositions-by-departure-date.md) for the provider-specific parameters and requirements.


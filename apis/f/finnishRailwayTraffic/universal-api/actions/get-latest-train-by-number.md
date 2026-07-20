# Finnish Railway Traffic: Get latest train by number

Retrieves the latest train by number from Finnish Railway Traffic.

```
GET https://connect.mindcloud.co/v1/universal/finnishRailwayTraffic/latest/actions/get-latest-train-by-number
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Finnish Railway Traffic `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/finnishRailwayTraffic/latest/actions/get-latest-train-by-number?connectionId=$CONNECTION_ID&trainNumber=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "trainNumber": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/finnishRailwayTraffic/latest/actions/get-latest-train-by-number?${params}`, {
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
| `trainNumber` | number | yes | Train number, for example 1. Default: `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cancelled": true,
      "commuterLineID": "string",
      "departureDate": "2026-05-07T12:00:00.000Z",
      "runningCurrently": true,
      "timeTableRows": [
        {}
      ],
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
| `cancelled` | boolean |  |
| `commuterLineID` | string |  |
| `departureDate` | date |  |
| `runningCurrently` | boolean |  |
| `timeTableRows` | array<object> |  |
| `trainCategory` | string |  |
| `trainNumber` | number |  |
| `trainType` | string |  |

## Native endpoint

Through the native Finnish Railway Traffic API, this operation is `GET /api/v1/trains/latest/:train_number` (base URL `https://rata.digitraffic.fi`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-latest-train-by-number.md) for the provider-specific parameters and requirements.


# Geocodio: Create Distance Job

Creates an asynchronous distance job in Geocodio.

```
POST https://connect.mindcloud.co/v1/universal/geocodio/latest/actions/create-distance-job
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Geocodio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/geocodio/latest/actions/create-distance-job" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Store to customer distances",
  "origins[]": "38.8977,-77.0365,WhiteHouse",
  "destinations[]": "38.8895,-77.0353,WashingtonMonument"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/geocodio/latest/actions/create-distance-job', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Store to customer distances",
    "origins[]": "38.8977,-77.0365,WhiteHouse",
    "destinations[]": "38.8895,-77.0353,WashingtonMonument"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | A name for the distance matrix job. Example: `Store to customer distances`. |
| `origins[]` | array<string> | yes | Origin list ID or array of coordinates/addresses. Example: `38.8977,-77.0365,WhiteHouse`. |
| `destinations[]` | array<string> | yes | Destination list ID or array of coordinates/addresses. Example: `38.8895,-77.0353,WashingtonMonument`. |
| `distanceMode` | string | no | Distance calculation mode: driving or straightline. One of: `0`, `1`. Default: `straightline`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `callbackUrl` | string | no | Optional webhook URL to call when the job completes. Example: `https://example.com/webhook/distance-complete`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "calculationsCompleted": 1,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "destinationsCount": 1,
      "destinationsType": "string",
      "distanceMode": "string",
      "downloadUrl": "https://example.com",
      "identifier": "string",
      "isExpired": true,
      "name": "Ava Chen",
      "originsCount": 1,
      "originsType": "string",
      "progress": 1,
      "status": "string",
      "statusMessage": "string",
      "timeLeft": "string",
      "totalCalculations": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `calculationsCompleted` | number | Completed calculations. |
| `createdAt` | date | Job creation time. |
| `destinationsCount` | number | Number of destination locations. |
| `destinationsType` | string | Type of destinations input. |
| `distanceMode` | string | Distance mode used by the job. |
| `downloadUrl` | string | Download URL when available. |
| `identifier` | string | Public job identifier. |
| `isExpired` | boolean | Whether the results have expired. |
| `name` | string | Job name. |
| `originsCount` | number | Number of origin locations. |
| `originsType` | string | Type of origins input. |
| `progress` | number | Completion percentage. |
| `status` | string | Job processing status. |
| `statusMessage` | string | Status message. |
| `timeLeft` | string | Estimated time remaining. |
| `totalCalculations` | number | Total calculations in the job. |

## Native endpoint

Through the native Geocodio API, this operation is `POST /distance-jobs` (base URL `https://api.geocod.io/v1.12`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-distance-job.md) for the provider-specific parameters and requirements.


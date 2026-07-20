# Geocodio: Get Distance Job

Retrieves an asynchronous distance job from Geocodio.

```
GET https://connect.mindcloud.co/v1/universal/geocodio/latest/actions/get-distance-job
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Geocodio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/geocodio/latest/actions/get-distance-job?connectionId=$CONNECTION_ID&identifier=abc123xyz" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "identifier": "abc123xyz"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/geocodio/latest/actions/get-distance-job?${params}`, {
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
| `identifier` | string | yes | Distance job identifier. Example: `abc123xyz`. |

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

Through the native Geocodio API, this operation is `GET /distance-jobs/{identifier}` (base URL `https://api.geocod.io/v1.12`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-distance-job.md) for the provider-specific parameters and requirements.


# Wodely: Search Routes



```
GET https://connect.mindcloud.co/v1/universal/wodely/latest/actions/search-routes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Wodely `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wodely/latest/actions/search-routes?connectionId=$CONNECTION_ID&startDateTime=2026-03-27T00%3A00%3A00Z&endDateTime=2026-03-27T23%3A59%3A59Z" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "startDateTime": "2026-03-27T00:00:00Z",
  "endDateTime": "2026-03-27T23:59:59Z"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/wodely/latest/actions/search-routes?${params}`, {
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
| `startDateTime` | string | yes | UTC ISO 8601 start of the route search window. Example: `2026-03-27T00:00:00Z`. |
| `endDateTime` | string | yes | UTC ISO 8601 end of the route search window. Example: `2026-03-27T23:59:59Z`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `routeId` | string | no | Optional route identifier to fetch a specific route. Example: `12345`. |
| `statusId` | string | no | Optional route status filter. Example: `pending`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "actualEndTime": "string",
      "actualStartTime": "string",
      "createdDateTime": "string",
      "distance": 1,
      "duration": 1,
      "endAddress": "string",
      "endCoordinates": "string",
      "endTime": "string",
      "id": 1,
      "routeName": "Ava Chen",
      "startAddress": "string",
      "startCoordinates": "string",
      "startTime": "string",
      "statusId": "string",
      "teamId": 1,
      "userFullName": "Ava Chen",
      "userId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `actualEndTime` | string | Actual route end time in UTC. |
| `actualStartTime` | string | Actual route start time in UTC. |
| `createdDateTime` | string | Route creation time in UTC. |
| `distance` | number | Route distance value returned by Wodely. |
| `duration` | number | Route duration value returned by Wodely. |
| `endAddress` | string | Route end address. |
| `endCoordinates` | string | Route end coordinates. |
| `endTime` | string | Planned route end time in UTC. |
| `id` | number | Route identifier. |
| `routeName` | string | Route name. |
| `startAddress` | string | Route start address. |
| `startCoordinates` | string | Route start coordinates. |
| `startTime` | string | Planned route start time in UTC. |
| `statusId` | string | Route status identifier. |
| `teamId` | number | Assigned team identifier. |
| `userFullName` | string | Assigned driver or worker full name. |
| `userId` | string | Assigned driver or worker user identifier. |

## Native endpoint

Through the native Wodely API, this operation is `POST /v2/routes/search` (base URL `https://api.wodely.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-routes.md) for the provider-specific parameters and requirements.


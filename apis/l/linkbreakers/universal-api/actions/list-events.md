# Linkbreakers: List Events

Retrieves a list of events from Linkbreakers.

```
GET https://connect.mindcloud.co/v1/universal/linkbreakers/latest/actions/list-events
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Linkbreakers `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/linkbreakers/latest/actions/list-events?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/linkbreakers/latest/actions/list-events?${params}`, {
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
| `linkId` | string | no | Filter events to a specific link. |
| `startDate` | date | no | Inclusive start timestamp for the query window. |
| `endDate` | date | no | Inclusive end timestamp for the query window. |
| `responseFormat` | string | no | Desired response format. |
| `include[]` | array<string> | no | Relationships to include in the response. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "csv": {
        "contentType": "string",
        "csvData": "string"
      },
      "json": {
        "events": [
          {
            "action": "string",
            "createdAt": "string",
            "destination": "string",
            "destinationAction": "string",
            "deviceId": "string",
            "entrypoint": "string",
            "httpMethod": "string",
            "id": "string",
            "linkId": "https://example.com",
            "scannedAt": "string",
            "traces": [
              {}
            ],
            "triggeredBy": "string",
            "updatedAt": "string",
            "visitorId": "string",
            "visitType": "string",
            "workspaceId": "string"
          }
        ],
        "hasMore": true,
        "nextPageToken": "string",
        "totalCount": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `csv` | object | CSV export payload when CSV format is requested. |
| `csv.contentType` | string |  |
| `csv.csvData` | string |  |
| `json` | object | Structured events response. |
| `json.events` | array<object> |  |
| `json.events[].action` | string |  |
| `json.events[].createdAt` | string |  |
| `json.events[].destination` | string |  |
| `json.events[].destinationAction` | string |  |
| `json.events[].deviceId` | string |  |
| `json.events[].entrypoint` | string |  |
| `json.events[].httpMethod` | string |  |
| `json.events[].id` | string |  |
| `json.events[].linkId` | string |  |
| `json.events[].scannedAt` | string |  |
| `json.events[].traces` | array<object> |  |
| `json.events[].triggeredBy` | string |  |
| `json.events[].updatedAt` | string |  |
| `json.events[].visitorId` | string |  |
| `json.events[].visitType` | string |  |
| `json.events[].workspaceId` | string |  |
| `json.hasMore` | boolean |  |
| `json.nextPageToken` | string |  |
| `json.totalCount` | number |  |

## Native endpoint

Through the native Linkbreakers API, this operation is `GET /v1/events` (base URL `https://api.linkbreakers.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-events.md) for the provider-specific parameters and requirements.


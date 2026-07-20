# Socket: List Historical Snapshots

Retrieves historical organization snapshots from Socket.

```
GET https://connect.mindcloud.co/v1/universal/socket/latest/actions/list-historical-snapshots
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Socket `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/socket/latest/actions/list-historical-snapshots?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/socket/latest/actions/list-historical-snapshots?${params}`, {
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
      "endCursor": "string",
      "items": [
        {
          "durationMs": 1,
          "finishedAt": "string",
          "id": "string",
          "numCriticalAlerts": 1,
          "numHighAlerts": 1,
          "numIgnoredCriticalAlerts": 1,
          "numIgnoredHighAlerts": 1,
          "numIgnoredLowAlerts": 1,
          "numIgnoredMediumAlerts": 1,
          "numLowAlerts": 1,
          "numMediumAlerts": 1,
          "numReposScanned": 1,
          "numSbomsScanned": 1,
          "requestedAt": "string",
          "requestedBy": "string",
          "requestId": "string",
          "startedAt": "string",
          "status": "string"
        }
      ],
      "meta": {
        "endDateInclusive": "string",
        "filters": {
          "requestId": [
            "string"
          ],
          "status": [
            "string"
          ]
        },
        "organizationId": "string",
        "queryStartTimestamp": 1,
        "startDateInclusive": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `endCursor` | string |  |
| `items` | array<object> |  |
| `items[]` | object |  |
| `items[].durationMs` | number |  |
| `items[].finishedAt` | string |  |
| `items[].id` | string |  |
| `items[].numCriticalAlerts` | number |  |
| `items[].numHighAlerts` | number |  |
| `items[].numIgnoredCriticalAlerts` | number |  |
| `items[].numIgnoredHighAlerts` | number |  |
| `items[].numIgnoredLowAlerts` | number |  |
| `items[].numIgnoredMediumAlerts` | number |  |
| `items[].numLowAlerts` | number |  |
| `items[].numMediumAlerts` | number |  |
| `items[].numReposScanned` | number |  |
| `items[].numSbomsScanned` | number |  |
| `items[].requestedAt` | string |  |
| `items[].requestedBy` | string |  |
| `items[].requestId` | string |  |
| `items[].startedAt` | string |  |
| `items[].status` | string |  |
| `meta` | object |  |
| `meta.endDateInclusive` | string |  |
| `meta.filters` | object |  |
| `meta.filters.requestId` | array<string> |  |
| `meta.filters.status` | array<string> |  |
| `meta.organizationId` | string |  |
| `meta.queryStartTimestamp` | number |  |
| `meta.startDateInclusive` | string |  |

## Native endpoint

Through the native Socket API, this operation is `GET /orgs/:org_slug/historical/snapshots` (base URL `https://api.socket.dev/v0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-historical-snapshots.md) for the provider-specific parameters and requirements.


# FireHydrant: List Incident Events

Retrieves incident events from FireHydrant.

```
GET https://connect.mindcloud.co/v1/universal/fireHydrant/latest/actions/list-incident-events
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FireHydrant `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fireHydrant/latest/actions/list-incident-events?connectionId=$CONNECTION_ID&limit=25&offset=0&incidentId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "incidentId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fireHydrant/latest/actions/list-incident-events?${params}`, {
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
| `incidentId` | string | yes | The FireHydrant incident ID. |
| `types` | string | no | Filter event types. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {
          "author": {},
          "context": "string",
          "conversations": [
            {}
          ],
          "data": {},
          "id": "string",
          "incidentId": "string",
          "occurredAt": "2026-05-07T12:00:00.000Z",
          "type": "string",
          "visibility": "string",
          "votes": {}
        }
      ],
      "pagination": {
        "count": 1,
        "items": 1,
        "last": 1,
        "page": 1,
        "pages": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data[].author` | object |  |
| `data[].context` | string |  |
| `data[].conversations` | array<object> |  |
| `data[].data` | object |  |
| `data[].id` | string |  |
| `data[].incidentId` | string |  |
| `data[].occurredAt` | date |  |
| `data[].type` | string |  |
| `data[].visibility` | string |  |
| `data[].votes` | object |  |
| `pagination.count` | number |  |
| `pagination.items` | number |  |
| `pagination.last` | number |  |
| `pagination.page` | number |  |
| `pagination.pages` | number |  |

## Native endpoint

Through the native FireHydrant API, this operation is `GET /incidents/:incident_id/events` (base URL `https://api.firehydrant.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-incident-events.md) for the provider-specific parameters and requirements.


# Mihu AI: Get Paginated List of Calls



```
GET https://connect.mindcloud.co/v1/universal/mihuAI/latest/actions/get-paginated-list-of-calls
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mihu AI `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mihuAI/latest/actions/get-paginated-list-of-calls?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mihuAI/latest/actions/get-paginated-list-of-calls?${params}`, {
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
| `agentId` | string | no | Filter calls by agent UUID. |
| `direction` | string | no | Filter calls by call direction. |
| `page` | number | no | Page number to return. |
| `perPage` | number | no | Number of records to return per page. |
| `status` | string | no | Filter calls by status. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "agent": {
        "name": "Ava Chen",
        "uuid": "string"
      },
      "analysis": "string",
      "communication": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "direction": "string",
      "duration": 1,
      "handledBy": "string",
      "status": "string",
      "timestamp": "2026-05-07T12:00:00.000Z",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `agent.name` | string |  |
| `agent.uuid` | string |  |
| `analysis` | string |  |
| `communication` | string |  |
| `createdAt` | date |  |
| `direction` | string |  |
| `duration` | number |  |
| `handledBy` | string |  |
| `status` | string |  |
| `timestamp` | date |  |
| `updatedAt` | date |  |
| `uuid` | string |  |

## Native endpoint

Through the native Mihu AI API, this operation is `GET /api/v1/calls` (base URL `https://{{credentials.subdomain}}.mindhunters.ai`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-paginated-list-of-calls.md) for the provider-specific parameters and requirements.


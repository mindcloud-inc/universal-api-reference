# Mihu AI: Get Paginated List of Tasks



```
GET https://connect.mindcloud.co/v1/universal/mihuAI/latest/actions/get-paginated-list-of-tasks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mihu AI `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mihuAI/latest/actions/get-paginated-list-of-tasks?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mihuAI/latest/actions/get-paginated-list-of-tasks?${params}`, {
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
| `agentUuid` | string | no |  |
| `campaignUuid` | string | no |  |
| `contactUuid` | string | no |  |
| `page` | number | no |  |
| `perPage` | number | no |  |
| `priority` | number | no |  |
| `scheduledFrom` | string | no |  |
| `scheduledTo` | string | no |  |
| `status` | string | no |  |
| `type` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "agentUuid": "string",
      "autoQueue": true,
      "campaignUuid": "string",
      "contactUuid": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "priority": 1,
      "scheduledAt": "2026-05-07T12:00:00.000Z",
      "status": "string",
      "timezone": "string",
      "title": "string",
      "type": "string",
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
| `agentUuid` | string |  |
| `autoQueue` | boolean |  |
| `campaignUuid` | string |  |
| `contactUuid` | string |  |
| `createdAt` | date |  |
| `description` | string |  |
| `priority` | number |  |
| `scheduledAt` | date |  |
| `status` | string |  |
| `timezone` | string |  |
| `title` | string |  |
| `type` | string |  |
| `updatedAt` | date |  |
| `uuid` | string |  |

## Native endpoint

Through the native Mihu AI API, this operation is `GET /api/v1/tasks` (base URL `https://{{credentials.subdomain}}.mindhunters.ai`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-paginated-list-of-tasks.md) for the provider-specific parameters and requirements.


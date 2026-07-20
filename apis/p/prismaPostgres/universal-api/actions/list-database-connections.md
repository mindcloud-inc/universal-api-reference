# Prisma Postgres: List Database Connections

Retrieves database connections from Prisma Postgres.

```
GET https://connect.mindcloud.co/v1/universal/prismaPostgres/latest/actions/list-database-connections
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Prisma Postgres `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/prismaPostgres/latest/actions/list-database-connections?connectionId=$CONNECTION_ID&limit=25&offset=0&databaseId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "databaseId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/prismaPostgres/latest/actions/list-database-connections?${params}`, {
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
| `databaseId` | string | yes | Database identifier. |
| `cursor` | string | no |  |
| `limit` | number | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "database": {},
      "directConnection": {},
      "endpoints": [
        {}
      ],
      "id": "string",
      "kind": "string",
      "name": "Ava Chen",
      "type": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `database` | object |  |
| `directConnection` | object |  |
| `endpoints` | array<object> |  |
| `id` | string |  |
| `kind` | string |  |
| `name` | string |  |
| `type` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Prisma Postgres API, this operation is `GET /databases/{databaseId}/connections` (base URL `https://api.prisma.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-database-connections.md) for the provider-specific parameters and requirements.


# Prisma Postgres: Create Database Connection String

Creates a database connection string in Prisma Postgres.

```
POST https://connect.mindcloud.co/v1/universal/prismaPostgres/latest/actions/create-database-connection-string
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Prisma Postgres `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/prismaPostgres/latest/actions/create-database-connection-string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "databaseId": "string",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/prismaPostgres/latest/actions/create-database-connection-string', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "databaseId": "string",
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `databaseId` | string | yes | Database identifier. |
| `name` | string | yes | Display name for the generated connection string. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "connectionString": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "database": {},
      "directConnection": {},
      "endpoints": [
        {}
      ],
      "host": "string",
      "id": "string",
      "kind": "string",
      "name": "Ava Chen",
      "pass": "string",
      "type": "string",
      "url": "https://example.com",
      "user": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `connectionString` | string |  |
| `createdAt` | date |  |
| `database` | object |  |
| `directConnection` | object |  |
| `endpoints` | array<object> |  |
| `host` | string |  |
| `id` | string |  |
| `kind` | string |  |
| `name` | string |  |
| `pass` | string |  |
| `type` | string |  |
| `url` | string |  |
| `user` | string |  |

## Native endpoint

Through the native Prisma Postgres API, this operation is `POST /databases/{databaseId}/connections` (base URL `https://api.prisma.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-database-connection-string.md) for the provider-specific parameters and requirements.


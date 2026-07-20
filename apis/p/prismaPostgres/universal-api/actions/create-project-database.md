# Prisma Postgres: Create Project Database

Creates a new project database in Prisma Postgres.

```
POST https://connect.mindcloud.co/v1/universal/prismaPostgres/latest/actions/create-project-database
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Prisma Postgres `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/prismaPostgres/latest/actions/create-project-database" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "projectId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/prismaPostgres/latest/actions/create-project-database', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "projectId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `projectId` | string | yes | Project that will own the new database. |
| `name` | string | no | Display name for the project database. |
| `region` | list | no | Target region for the new project database. |
| `isDefault` | boolean | no | Whether the project database should become default. |
| `fromDatabase` | object | no |  |
| `source` | object | no | Optional source object to create the project database from. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "apiKeys": [
        {}
      ],
      "connections": [
        {}
      ],
      "connectionString": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "defaultConnectionId": "string",
      "directConnection": {},
      "id": "string",
      "isDefault": true,
      "name": "Ava Chen",
      "project": {},
      "region": {},
      "source": {},
      "status": "string",
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
| `apiKeys` | array<object> |  |
| `connections` | array<object> |  |
| `connectionString` | string |  |
| `createdAt` | date |  |
| `defaultConnectionId` | string |  |
| `directConnection` | object |  |
| `id` | string |  |
| `isDefault` | boolean |  |
| `name` | string |  |
| `project` | object |  |
| `region` | object |  |
| `source` | object |  |
| `status` | string |  |
| `type` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Prisma Postgres API, this operation is `POST /projects/{projectId}/databases` (base URL `https://api.prisma.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-project-database.md) for the provider-specific parameters and requirements.


# Prisma Postgres: Create Database

Creates a new database in Prisma Postgres.

```
POST https://connect.mindcloud.co/v1/universal/prismaPostgres/latest/actions/create-database
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Prisma Postgres `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/prismaPostgres/latest/actions/create-database" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "projectId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/prismaPostgres/latest/actions/create-database', {
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
| `isDefault` | boolean | no | Whether the created database should become the project default. |
| `name` | string | no | Display name for the new database. |
| `projectId` | string | yes | Project that will own the new database. |
| `region` | list | no | Target region for the database. Use inherit to follow the project default. |
| `source` | object | no | Optional source object to create the database from. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "connections": [
        {}
      ],
      "createdAt": "2026-05-07T12:00:00.000Z",
      "defaultConnectionId": "string",
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
| `connections` | array<object> |  |
| `createdAt` | date |  |
| `defaultConnectionId` | string |  |
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

Through the native Prisma Postgres API, this operation is `POST /databases` (base URL `https://api.prisma.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-database.md) for the provider-specific parameters and requirements.


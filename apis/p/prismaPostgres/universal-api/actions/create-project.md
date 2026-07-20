# Prisma Postgres: Create Project

Creates a new project in Prisma Postgres.

```
POST https://connect.mindcloud.co/v1/universal/prismaPostgres/latest/actions/create-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Prisma Postgres `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/prismaPostgres/latest/actions/create-project" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/prismaPostgres/latest/actions/create-project', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `createDatabase` | boolean | no | Whether Prisma should create a default database with the new project. |
| `name` | string | no | Display name for the new project. |
| `region` | list | no | Project region. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "database": {},
      "defaultRegion": "string",
      "id": "string",
      "name": "Ava Chen",
      "type": "string",
      "url": "https://example.com",
      "workspace": {}
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
| `defaultRegion` | string |  |
| `id` | string |  |
| `name` | string |  |
| `type` | string |  |
| `url` | string |  |
| `workspace` | object |  |

## Native endpoint

Through the native Prisma Postgres API, this operation is `POST /projects` (base URL `https://api.prisma.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-project.md) for the provider-specific parameters and requirements.


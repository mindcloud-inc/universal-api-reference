# Prisma Postgres: List Databases

Retrieves databases from Prisma Postgres.

```
GET https://connect.mindcloud.co/v1/universal/prismaPostgres/latest/actions/list-databases
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Prisma Postgres `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/prismaPostgres/latest/actions/list-databases?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/prismaPostgres/latest/actions/list-databases?${params}`, {
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
| `projectId` | string | no | Optional project to filter returned databases by. |
| `cursor` | string | no |  |
| `limit` | number | no |  |

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

Through the native Prisma Postgres API, this operation is `GET /databases` (base URL `https://api.prisma.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-databases.md) for the provider-specific parameters and requirements.


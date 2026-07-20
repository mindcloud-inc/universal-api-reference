# Prisma Postgres: Get Database

Retrieves a database from Prisma Postgres.

```
GET https://connect.mindcloud.co/v1/universal/prismaPostgres/latest/actions/get-database
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Prisma Postgres `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/prismaPostgres/latest/actions/get-database?connectionId=$CONNECTION_ID&databaseId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "databaseId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/prismaPostgres/latest/actions/get-database?${params}`, {
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

Through the native Prisma Postgres API, this operation is `GET /databases/{databaseId}` (base URL `https://api.prisma.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-database.md) for the provider-specific parameters and requirements.


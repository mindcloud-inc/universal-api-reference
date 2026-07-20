# Prisma Postgres: List Database Backups

Retrieves database backups from Prisma Postgres.

```
GET https://connect.mindcloud.co/v1/universal/prismaPostgres/latest/actions/list-database-backups
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Prisma Postgres `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/prismaPostgres/latest/actions/list-database-backups?connectionId=$CONNECTION_ID&databaseId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "databaseId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/prismaPostgres/latest/actions/list-database-backups?${params}`, {
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
| `limit` | number | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "backupType": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "size": 1,
      "status": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `backupType` | string |  |
| `createdAt` | date |  |
| `id` | string |  |
| `size` | number |  |
| `status` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Prisma Postgres API, this operation is `GET /databases/{databaseId}/backups` (base URL `https://api.prisma.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-database-backups.md) for the provider-specific parameters and requirements.


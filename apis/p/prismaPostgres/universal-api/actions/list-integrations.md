# Prisma Postgres: List Integrations

Retrieves integrations from Prisma Postgres.

```
GET https://connect.mindcloud.co/v1/universal/prismaPostgres/latest/actions/list-integrations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Prisma Postgres `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/prismaPostgres/latest/actions/list-integrations?connectionId=$CONNECTION_ID&limit=25&offset=0&workspaceId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "workspaceId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/prismaPostgres/latest/actions/list-integrations?${params}`, {
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
| `workspaceId` | string | yes | Workspace whose integrations should be listed. |
| `cursor` | string | no |  |
| `limit` | number | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "client": {},
      "createdAt": "2026-05-07T12:00:00.000Z",
      "createdByUser": {},
      "id": "string",
      "scopes": [
        "string"
      ],
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `client` | object |  |
| `createdAt` | date |  |
| `createdByUser` | object |  |
| `id` | string |  |
| `scopes` | array<string> |  |
| `url` | string |  |

## Native endpoint

Through the native Prisma Postgres API, this operation is `GET /integrations` (base URL `https://api.prisma.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-integrations.md) for the provider-specific parameters and requirements.


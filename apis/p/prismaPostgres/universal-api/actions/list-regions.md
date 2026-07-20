# Prisma Postgres: List Regions

Retrieves regions from Prisma Postgres.

```
GET https://connect.mindcloud.co/v1/universal/prismaPostgres/latest/actions/list-regions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Prisma Postgres `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/prismaPostgres/latest/actions/list-regions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/prismaPostgres/latest/actions/list-regions?${params}`, {
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
| `product` | list | no | Optional product filter for regions. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "name": "Ava Chen",
      "product": "string",
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
| `id` | string |  |
| `name` | string |  |
| `product` | string |  |
| `status` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Prisma Postgres API, this operation is `GET /regions` (base URL `https://api.prisma.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-regions.md) for the provider-specific parameters and requirements.


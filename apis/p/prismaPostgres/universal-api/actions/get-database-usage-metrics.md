# Prisma Postgres: Get Database Usage Metrics

Retrieves database usage metrics from Prisma Postgres.

```
GET https://connect.mindcloud.co/v1/universal/prismaPostgres/latest/actions/get-database-usage-metrics
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Prisma Postgres `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/prismaPostgres/latest/actions/get-database-usage-metrics?connectionId=$CONNECTION_ID&databaseId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "databaseId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/prismaPostgres/latest/actions/get-database-usage-metrics?${params}`, {
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
| `endDate` | date | no | End of the usage window. |
| `startDate` | date | no | Start of the usage window. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "generatedAt": "2026-05-07T12:00:00.000Z",
      "metrics": {},
      "period": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `generatedAt` | date |  |
| `metrics` | object |  |
| `period` | object |  |

## Native endpoint

Through the native Prisma Postgres API, this operation is `GET /databases/{databaseId}/usage` (base URL `https://api.prisma.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-database-usage-metrics.md) for the provider-specific parameters and requirements.


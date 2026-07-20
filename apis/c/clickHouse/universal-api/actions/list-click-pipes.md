# ClickHouse: List ClickPipes



```
GET https://connect.mindcloud.co/v1/universal/clickHouse/latest/actions/list-click-pipes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ClickHouse `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clickHouse/latest/actions/list-click-pipes?connectionId=$CONNECTION_ID&organizationId=string&serviceId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "organizationId": "string",
  "serviceId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clickHouse/latest/actions/list-click-pipes?${params}`, {
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
| `organizationId` | string | yes | ID of the organization that owns the service. |
| `serviceId` | string | yes | ID of the requested service. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "destination": {},
      "fieldMappings": [
        {}
      ],
      "id": "string",
      "name": "Ava Chen",
      "scaling": {},
      "serviceId": "string",
      "settings": {},
      "source": {},
      "state": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date | ClickPipe creation timestamp. |
| `destination` | object | ClickPipe destination configuration. |
| `fieldMappings` | array<object> | ClickPipe field mappings. |
| `id` | string | Unique ClickPipe ID. |
| `name` | string | ClickPipe name. |
| `scaling` | object | ClickPipe scaling configuration. |
| `serviceId` | string | Service ID this ClickPipe belongs to. |
| `settings` | object | ClickPipe settings. |
| `source` | object | ClickPipe source configuration. |
| `state` | string | Current lifecycle state of the ClickPipe. |
| `updatedAt` | date | ClickPipe last update timestamp. |

## Native endpoint

Through the native ClickHouse API, this operation is `GET /v1/organizations/[:organizationId]/services/[:serviceId]/clickpipes` (base URL `https://api.clickhouse.cloud`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-click-pipes.md) for the provider-specific parameters and requirements.


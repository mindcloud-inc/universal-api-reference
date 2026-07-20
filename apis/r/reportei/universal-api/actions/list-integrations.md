# Reportei: List Integrations

Retrieves integrations from Reportei.

```
GET https://connect.mindcloud.co/v1/universal/reportei/latest/actions/list-integrations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Reportei `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/reportei/latest/actions/list-integrations?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/reportei/latest/actions/list-integrations?${params}`, {
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
| `projectId` | number | no | Filtrar por projeto específico. |
| `name` | string | no | Filtrar pelo nome da integração. |
| `slug` | string | no | Filtrar pelo tipo de integração. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {
          "id": 1,
          "name": "Ava Chen",
          "slug": "string",
          "status": "string"
        }
      ],
      "meta": {
        "total": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data[].id` | number | Integration identifier |
| `data[].name` | string | Integration name |
| `data[].slug` | string | Integration slug |
| `data[].status` | string | Integration status |
| `meta.total` | number | Total number of integrations |

## Native endpoint

Through the native Reportei API, this operation is `GET /integrations` (base URL `https://app.reportei.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-integrations.md) for the provider-specific parameters and requirements.


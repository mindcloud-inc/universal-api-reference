# Reportei: List Reports

Retrieves reports from Reportei.

```
GET https://connect.mindcloud.co/v1/universal/reportei/latest/actions/list-reports
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Reportei `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/reportei/latest/actions/list-reports?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/reportei/latest/actions/list-reports?${params}`, {
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
| `createdAt` | date | no | Filtrar por data de criação. |
| `updatedAt` | date | no | Filtrar por data de atualização. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {
          "external_url": "https://example.com",
          "id": 1,
          "subtitle": "string",
          "title": "string"
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
| `data[].external_url` | string | Public report URL |
| `data[].id` | number | Report identifier |
| `data[].subtitle` | string | Report subtitle |
| `data[].title` | string | Report title |
| `meta.total` | number | Total number of reports |

## Native endpoint

Through the native Reportei API, this operation is `GET /reports` (base URL `https://app.reportei.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-reports.md) for the provider-specific parameters and requirements.


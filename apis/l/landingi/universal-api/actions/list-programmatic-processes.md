# Landingi: List Programmatic Processes

Retrieves programmatic landing page processes from Landingi.

```
GET https://connect.mindcloud.co/v1/universal/landingi/latest/actions/list-programmatic-processes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Landingi `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/landingi/latest/actions/list-programmatic-processes?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/landingi/latest/actions/list-programmatic-processes?${params}`, {
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
| `filters` | object | no |  |
| `filters.query` | string | no | Search by process name. |
| `filters.sourceUuid` | string | no | Filter by the source landing page UUID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "string",
      "errors": 1,
      "identifier": "string",
      "name": "Ava Chen",
      "processed": 1,
      "source_archived": true,
      "source_uuid": "string",
      "status": "string",
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | string | Process creation timestamp. |
| `errors` | number | Number of landing pages that failed. |
| `identifier` | string | Programmatic process identifier. |
| `name` | string | Programmatic process name. |
| `processed` | number | Number of processed landing pages. |
| `source_archived` | boolean | Whether the source landing page is archived. |
| `source_uuid` | string | Source landing page UUID. |
| `status` | string | Current process status. |
| `total` | number | Total landing pages in the process. |

## Native endpoint

Through the native Landingi API, this operation is `GET /landing-page/programmatic/processes` (base URL `https://api.landingi.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-programmatic-processes.md) for the provider-specific parameters and requirements.


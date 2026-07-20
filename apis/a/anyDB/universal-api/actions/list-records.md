# AnyDB: List Records

Retrieves records from AnyDB with optional filters and pagination.

```
GET https://connect.mindcloud.co/v1/universal/anyDB/latest/actions/list-records
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AnyDB `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/anyDB/latest/actions/list-records?connectionId=$CONNECTION_ID&teamId=string&databaseId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "teamId": "string",
  "databaseId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/anyDB/latest/actions/list-records?${params}`, {
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
| `teamId` | string | yes | The AnyDB team ID. |
| `databaseId` | string | yes | The AnyDB database ID. |
| `groupBy` | string | no | Optional AnyDB group-by field. |
| `templateId` | string | no | Optional template ID to filter by. |
| `templateName` | string | no | Optional template name to filter by. |
| `parentId` | string | no | Optional parent record ID to scope the listing. |
| `pageSize` | number | no | Optional page size for the listing. |
| `lastMarker` | string | no | Optional pagination marker from a previous response. |
| `sort` | string | no | Optional JSON string describing AnyDB sort instructions. |
| `filter` | string | no | Optional JSON string describing AnyDB filter rules. |
| `previewCells` | string | no | Optional JSON string describing which cells to preview. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native AnyDB API returns.

## Native endpoint

Through the native AnyDB API, this operation is `GET /api/integrations/ext/list` (base URL `https://app.anydb.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-records.md) for the provider-specific parameters and requirements.


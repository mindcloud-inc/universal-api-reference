# SingleStore: List Available Tables with Selection Status

Retrieves available source tables and their ingestion selection status from SingleStore.

```
GET https://connect.mindcloud.co/v1/universal/singleStore/latest/actions/list-available-tables-with-selection-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SingleStore `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/singleStore/latest/actions/list-available-tables-with-selection-status?connectionId=$CONNECTION_ID&database=string&schema=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "database": "string",
  "schema": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/singleStore/latest/actions/list-available-tables-with-selection-status?${params}`, {
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
| `database` | string | yes | Database name in the source system. |
| `schema` | string | yes | Schema name inside the selected database. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "name": "Ava Chen",
      "selected": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | Table identifier returned by the API. |
| `name` | string | Table name. |
| `selected` | boolean | Whether the table is currently selected for ingestion. |

## Native endpoint

Through the native SingleStore API, this operation is `GET /list-db/{database}/{schema}` (base URL `https://{{credentials.flowEndpoint}}:30081/ingest/api/ingest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-available-tables-with-selection-status.md) for the provider-specific parameters and requirements.


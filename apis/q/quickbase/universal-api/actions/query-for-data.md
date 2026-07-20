# Quickbase: Query for Data

Queries records from a Quickbase table.

```
GET https://connect.mindcloud.co/v1/universal/quickbase/latest/actions/query-for-data
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Quickbase `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/quickbase/latest/actions/query-for-data?connectionId=$CONNECTION_ID&from=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "from": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/quickbase/latest/actions/query-for-data?${params}`, {
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
| `from` | string | yes | The Quickbase table identifier to query. |
| `select[]` | array<number> | no | Optional array of Quickbase field IDs to return. Leave empty to use the table's default columns. |
| `where` | string | no | Optional Quickbase query-language filter string, for example {'6'.CT.'Acme'}. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `sortBy[]` | array<object> | no | Optional array of sort objects, each with fieldId and order. |
| `groupBy[]` | array<object> | no | Optional array of group objects, each with fieldId and grouping. |
| `options` | object | no | Optional object containing runQuery options such as top, skip, and compareWithAppLocalTime. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {}
      ],
      "fields": [
        {}
      ],
      "metadata": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> | The returned Quickbase records. |
| `fields` | array<object> | Metadata for the fields included in the result. |
| `metadata` | object | Result metadata including counts and pagination values. |

## Native endpoint

Through the native Quickbase API, this operation is `POST v1/records/query` (base URL `https://api.quickbase.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/query-for-data.md) for the provider-specific parameters and requirements.


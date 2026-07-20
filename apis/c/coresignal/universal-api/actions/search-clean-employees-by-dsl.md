# Coresignal: Search Clean Employees By DSL

Finds clean employees in Coresignal with an Elasticsearch DSL query.

```
GET https://connect.mindcloud.co/v1/universal/coresignal/latest/actions/search-clean-employees-by-dsl
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Coresignal `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/coresignal/latest/actions/search-clean-employees-by-dsl?connectionId=$CONNECTION_ID&query=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "[object Object]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/coresignal/latest/actions/search-clean-employees-by-dsl?${params}`, {
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
| `query` | object | yes | Elasticsearch DSL query object. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "value": [
        1
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `value` | array<number> | Array of matching employee IDs. |

## Native endpoint

Through the native Coresignal API, this operation is `POST /employee_clean/search/es_dsl` (base URL `https://api.coresignal.com/cdapi/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-clean-employees-by-dsl.md) for the provider-specific parameters and requirements.


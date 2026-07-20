# QuintaDB: Run Field Actions

Runs a field action on multiple QuintaDB records.

```
GET https://connect.mindcloud.co/v1/universal/quintaDB/latest/actions/run-field-actions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a QuintaDB `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/quintaDB/latest/actions/run-field-actions?connectionId=$CONNECTION_ID&action_property_id=string&json_dtype_ids=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "action_property_id": "string",
  "json_dtype_ids": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/quintaDB/latest/actions/run-field-actions?${params}`, {
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
| `action_property_id` | string | yes |  |
| `json_dtype_ids` | string | yes |  |
| `run_by_all_table_or_report` | string | no |  |
| `view` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "success": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | string | Multi-action-run confirmation returned by QuintaDB. |

## Native endpoint

Through the native QuintaDB API, this operation is `GET /actions/:action_property_id.json` (base URL `https://quintadb.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/run-field-actions.md) for the provider-specific parameters and requirements.


# Dashly: Import User Properties from CSV

Imports user properties into Dashly from CSV.

```
POST https://connect.mindcloud.co/v1/universal/dashly/latest/actions/import-user-properties-from-csv
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dashly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/dashly/latest/actions/import-user-properties-from-csv" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "csvContent": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dashly/latest/actions/import-user-properties-from-csv', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "csvContent": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `csvContent` | string | yes | CSV file contents including the header row. |
| `mergeField` | string | no | Default: `$user_id`. |
| `delimiter` | string | no | Default: `;`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `filename` | string | no | Default: `dashly-import.csv`. |
| `tags` | string | no | Dashly tags payload, for example "\"super_tag\",\"import_tag_2\"". |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Dashly API returns.

## Native endpoint

Through the native Dashly API, this operation is `POST users/import` (base URL `https://api.dashly.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/import-user-properties-from-csv.md) for the provider-specific parameters and requirements.


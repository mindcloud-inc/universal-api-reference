# GoCanvas: Update Reference Data



```
PUT https://connect.mindcloud.co/v1/universal/goCanvas/latest/actions/update-reference-data
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GoCanvas `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/goCanvas/latest/actions/update-reference-data" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "referenceDataId": 1,
  "headers[]": [
    "string"
  ],
  "rows[]": [
    [
      "string"
    ]
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/goCanvas/latest/actions/update-reference-data', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "referenceDataId": 1,
    "headers[]": ["string"],
    "rows[]": [["string"]]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `referenceDataId` | number | yes |  |
| `headers[]` | array<string> | yes | Include gc_row_index to identify existing rows for updates. |
| `rows[]` | array<array> | yes | Rows with an existing gc_row_index update that row. A blank index, or omitting the index column, adds rows. |
| `deleteRows[]` | array<number> | no | Row indexes to delete. Retrieve the current dataset with Rows with Index first. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `publishToCustomers` | boolean | no | For partners: propagate updated reference data to customer accounts that have access. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native GoCanvas API returns.

## Native endpoint

Through the native GoCanvas API, this operation is `PATCH /reference_data/:referenceDataId` (base URL `https://www.gocanvas.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-reference-data.md) for the provider-specific parameters and requirements.


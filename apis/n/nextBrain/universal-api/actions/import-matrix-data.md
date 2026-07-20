# NextBrain: Import Matrix Data

Imports matrix data into a NextBrain dataset.

```
POST https://connect.mindcloud.co/v1/universal/nextBrain/latest/actions/import-matrix-data
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NextBrain `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/nextBrain/latest/actions/import-matrix-data" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "matrix[]": [
    [
      "string"
    ]
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/nextBrain/latest/actions/import-matrix-data', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "matrix[]": [["string"]]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `matrix[]` | array<array> | yes | A matrix where the first row is the header and each following row is data. |
| `workspaceId` | string | no | Optional workspace or project ID for the import target. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native NextBrain API returns.

## Native endpoint

Through the native NextBrain API, this operation is `POST /csv/import_matrix_token` (base URL `https://api.nextbrain.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/import-matrix-data.md) for the provider-specific parameters and requirements.


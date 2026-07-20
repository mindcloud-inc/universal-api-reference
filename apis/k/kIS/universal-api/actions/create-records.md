# KIS: Create Records

Creates one or more records in a KIS data table.

```
POST https://connect.mindcloud.co/v1/universal/kIS/latest/actions/create-records
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a KIS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/kIS/latest/actions/create-records" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "collectionName": "Ava Chen",
  "documents[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/kIS/latest/actions/create-records', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "collectionName": "Ava Chen",
    "documents[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `collectionName` | string | yes | Exact KIS table name where records should be created. |
| `documents[]` | array<object> | yes | Array of objects to create. Keys must match the KIS table field names exactly. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native KIS API returns.

## Native endpoint

Through the native KIS API, this operation is `POST /api_token_access/data_handlers` (base URL `https://api.getkis.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-records.md) for the provider-specific parameters and requirements.


# Sisense: Update Relation

Updates an existing relation in Sisense.

```
PUT https://connect.mindcloud.co/v1/universal/sisense/latest/actions/update-relation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sisense `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/sisense/latest/actions/update-relation" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sisense/latest/actions/update-relation', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `columns[].column` | string | no | The column oid for a related column. |
| `columns[].dataset` | string | no | The dataset oid for a related column. |
| `columns[].table` | string | no | The table oid for a related column. |
| `datamodelId` | string | no | The Datamodel oid. |
| `relationId` | string | no | The Relation oid. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Sisense API returns.

## Native endpoint

Through the native Sisense API, this operation is `PATCH /api/v2/datamodels/:datamodelId/relations/:relationId` (base URL `https://signup-126940n0.sisense.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-relation.md) for the provider-specific parameters and requirements.


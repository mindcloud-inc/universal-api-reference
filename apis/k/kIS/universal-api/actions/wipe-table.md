# KIS: Wipe Table

Deletes all records from a KIS data table.

```
DELETE https://connect.mindcloud.co/v1/universal/kIS/latest/actions/wipe-table
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a KIS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/kIS/latest/actions/wipe-table?connectionId=$CONNECTION_ID&tableId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "tableId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kIS/latest/actions/wipe-table?${params}`, {
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
| `tableId` | string | yes | KIS table object ID to wipe. Used in the request path. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native KIS API returns.

## Native endpoint

Through the native KIS API, this operation is `POST /api_token_access/collections/wipe/{tableId}` (base URL `https://api.getkis.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/wipe-table.md) for the provider-specific parameters and requirements.


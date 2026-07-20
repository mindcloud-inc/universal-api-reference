# SeaTable: Get Row

Retrieves a row from a SeaTable base.

```
GET https://connect.mindcloud.co/v1/universal/seaTable/latest/actions/get-row
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SeaTable `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/seaTable/latest/actions/get-row?connectionId=$CONNECTION_ID&rowId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "rowId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/seaTable/latest/actions/get-row?${params}`, {
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
| `rowId` | string | yes | The SeaTable row ID. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native SeaTable API returns.

## Native endpoint

Through the native SeaTable API, this operation is `GET /api-gateway/api/v2/dtables/:base_uuid/rows/:row_id/` (base URL `https://cloud.seatable.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-row.md) for the provider-specific parameters and requirements.


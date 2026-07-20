# QuintaDB: Get Relation Field ID

Retrieves a relation field ID from QuintaDB.

```
GET https://connect.mindcloud.co/v1/universal/quintaDB/latest/actions/get-relation-field-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a QuintaDB `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/quintaDB/latest/actions/get-relation-field-id?connectionId=$CONNECTION_ID&entity_id=string&property_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "entity_id": "string",
  "property_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/quintaDB/latest/actions/get-relation-field-id?${params}`, {
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
| `entity_id` | string | yes |  |
| `property_id` | string | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native QuintaDB API returns.

## Native endpoint

Through the native QuintaDB API, this operation is `GET /entities/:entity_id/get_rel_id/:property_id.json` (base URL `https://quintadb.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-relation-field-id.md) for the provider-specific parameters and requirements.


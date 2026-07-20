# QuintaDB: Delete Field

Deletes an existing field from QuintaDB.

```
DELETE https://connect.mindcloud.co/v1/universal/quintaDB/latest/actions/delete-field
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a QuintaDB `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/quintaDB/latest/actions/delete-field?connectionId=$CONNECTION_ID&app_id=string&entity_id=string&property_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "app_id": "string",
  "entity_id": "string",
  "property_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/quintaDB/latest/actions/delete-field?${params}`, {
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
| `app_id` | string | yes |  |
| `entity_id` | string | yes |  |
| `property_id` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "fields": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `fields` | array<object> | Remaining QuintaDB fields after deletion. |

## Native endpoint

Through the native QuintaDB API, this operation is `DELETE /apps/:app_id/entities/:entity_id/properties/:property_id.json` (base URL `https://quintadb.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-field.md) for the provider-specific parameters and requirements.


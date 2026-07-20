# QuintaDB: Create Field

Creates a new field in QuintaDB.

```
POST https://connect.mindcloud.co/v1/universal/quintaDB/latest/actions/create-field
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a QuintaDB `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/quintaDB/latest/actions/create-field" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "app_id": "string",
  "entity_id": "string",
  "name": "Ava Chen",
  "type_name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/quintaDB/latest/actions/create-field', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "app_id": "string",
    "entity_id": "string",
    "name": "Ava Chen",
    "type_name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `app_id` | string | yes |  |
| `entity_id` | string | yes |  |
| `name` | string | yes |  |
| `type_name` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "field": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `field` | object | Created QuintaDB field. |

## Native endpoint

Through the native QuintaDB API, this operation is `POST /apps/:app_id/entities/:entity_id/properties.json` (base URL `https://quintadb.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-field.md) for the provider-specific parameters and requirements.


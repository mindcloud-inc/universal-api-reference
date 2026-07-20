# QuintaDB: List Fields

Retrieves all fields from a QuintaDB form.

```
GET https://connect.mindcloud.co/v1/universal/quintaDB/latest/actions/list-fields
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a QuintaDB `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/quintaDB/latest/actions/list-fields?connectionId=$CONNECTION_ID&app_id=string&entity_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "app_id": "string",
  "entity_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/quintaDB/latest/actions/list-fields?${params}`, {
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
| `fields` | array<object> | Fields that belong to the specified form. |

## Native endpoint

Through the native QuintaDB API, this operation is `GET /apps/:app_id/entities/:entity_id/properties.json` (base URL `https://quintadb.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-fields.md) for the provider-specific parameters and requirements.


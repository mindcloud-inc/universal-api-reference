# Kontent.ai: Upsert management content item

Upserts a content item in Kontent.ai.

```
PUT https://connect.mindcloud.co/v1/universal/kontentai/latest/actions/upsert-management-content-item
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kontent.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/kontentai/latest/actions/upsert-management-content-item" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "itemIdentifier": "string",
  "body": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/kontentai/latest/actions/upsert-management-content-item', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "itemIdentifier": "string",
    "body": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `itemIdentifier` | string | yes | Kontent.ai content item identifier to upsert. |
| `body` | object | yes | JSON request body for upserting a Kontent.ai management content item. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "codename": "Ava Chen",
      "collection": {
        "id": "string"
      },
      "external_id": "string",
      "id": "string",
      "last_modified": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "type": {
        "id": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `codename` | string | Content item codename. |
| `collection.id` | string | Collection ID. |
| `external_id` | string | External ID. |
| `id` | string | Content item ID. |
| `last_modified` | date | Last modified timestamp. |
| `name` | string | Content item name. |
| `type.id` | string | Content type ID. |

## Native endpoint

Through the native Kontent.ai API, this operation is `PUT https://manage.kontent.ai/v2/projects/:environment_id/items/:item_identifier` (base URL `https://deliver.kontent.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upsert-management-content-item.md) for the provider-specific parameters and requirements.


# Kontent.ai: List management content items

Retrieves content items from your Kontent.ai environment.

```
GET https://connect.mindcloud.co/v1/universal/kontentai/latest/actions/list-management-content-items
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kontent.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kontentai/latest/actions/list-management-content-items?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kontentai/latest/actions/list-management-content-items?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



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

Through the native Kontent.ai API, this operation is `GET https://manage.kontent.ai/v2/projects/:environment_id/items` (base URL `https://deliver.kontent.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-management-content-items.md) for the provider-specific parameters and requirements.


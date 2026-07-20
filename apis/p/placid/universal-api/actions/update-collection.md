# Placid: Update Collection

Updates an existing collection in Placid.

```
PUT https://connect.mindcloud.co/v1/universal/placid/latest/actions/update-collection
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Placid `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/placid/latest/actions/update-collection" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "collectionId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/placid/latest/actions/update-collection', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "collectionId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `collectionId` | string | yes | ID of the collection to update. |
| `title` | string | no | Updated title for the collection. |
| `templateUuids[]` | array<string> | no | Full list of template UUIDs that should remain in the collection. |
| `addTemplateUuids[]` | array<string> | no | Template UUIDs to add to the collection. |
| `removeTemplateUuids[]` | array<string> | no | Template UUIDs to remove from the collection. |
| `customData` | object | no | Updated custom data for the collection. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "customData": "string",
      "id": "string",
      "templates": [
        "string"
      ],
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `customData` | string |  |
| `id` | string |  |
| `templates` | array<string> |  |
| `title` | string |  |

## Native endpoint

Through the native Placid API, this operation is `PATCH /api/rest/collections/:collectionId` (base URL `https://api.placid.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-collection.md) for the provider-specific parameters and requirements.


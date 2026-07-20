# LinkTwin: Bulk Assign Links To Collection

Adds or removes multiple links for a collection in LinkTwin.

```
PUT https://connect.mindcloud.co/v1/universal/linkTwin/latest/actions/bulk-assign-links-to-collection
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LinkTwin `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/linkTwin/latest/actions/bulk-assign-links-to-collection" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/linkTwin/latest/actions/bulk-assign-links-to-collection', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Collection ID. |
| `add[]` | array<number> | no | Link IDs to add. |
| `remove[]` | array<number> | no | Link IDs to remove. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "added": [
        1
      ],
      "collectionId": 1,
      "error": 1,
      "removed": [
        1
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `added[]` | number |  |
| `collectionId` | number |  |
| `error` | number |  |
| `removed[]` | number |  |

## Native endpoint

Through the native LinkTwin API, this operation is `POST /collection/:id/links` (base URL `https://linktw.in/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/bulk-assign-links-to-collection.md) for the provider-specific parameters and requirements.


# LinkTwin: Update Collection

Updates an existing collection in LinkTwin.

```
PUT https://connect.mindcloud.co/v1/universal/linkTwin/latest/actions/update-collection
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LinkTwin `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/linkTwin/latest/actions/update-collection" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/linkTwin/latest/actions/update-collection', {
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
| `name` | string | no | Collection name. |
| `slug` | string | no | Rotator slug. |
| `description` | string | no | Collection description. |
| `color` | string | no | Collection badge color in HEX. |
| `public` | boolean | no | Whether the collection is public. |
| `starred` | boolean | no | Whether the collection is starred. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "collection": "string",
      "color": "string",
      "description": "string",
      "error": 1,
      "id": 1,
      "list": "string",
      "public": true,
      "rotator": "string",
      "starred": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `collection` | string |  |
| `color` | string |  |
| `description` | string |  |
| `error` | number |  |
| `id` | number |  |
| `list` | string |  |
| `public` | boolean |  |
| `rotator` | string |  |
| `starred` | boolean |  |

## Native endpoint

Through the native LinkTwin API, this operation is `PUT /collection/:id/update` (base URL `https://linktw.in/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-collection.md) for the provider-specific parameters and requirements.


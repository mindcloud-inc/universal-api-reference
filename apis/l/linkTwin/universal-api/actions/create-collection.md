# LinkTwin: Create Collection

Creates a new collection in LinkTwin.

```
POST https://connect.mindcloud.co/v1/universal/linkTwin/latest/actions/create-collection
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LinkTwin `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/linkTwin/latest/actions/create-collection" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/linkTwin/latest/actions/create-collection', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Collection name. |
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
      "list": true,
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
| `list` | boolean |  |
| `public` | boolean |  |
| `rotator` | string |  |
| `starred` | boolean |  |

## Native endpoint

Through the native LinkTwin API, this operation is `POST /collection/add` (base URL `https://linktw.in/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-collection.md) for the provider-specific parameters and requirements.


# LinkTwin: Get Collection

Retrieves a collection and its items from LinkTwin.

```
GET https://connect.mindcloud.co/v1/universal/linkTwin/latest/actions/get-collection
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LinkTwin `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/linkTwin/latest/actions/get-collection?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/linkTwin/latest/actions/get-collection?${params}`, {
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
| `id` | string | yes | Collection ID. |
| `limit` | number | no | Per page data result. |
| `page` | number | no | Current page request. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "collection": {
        "clicks": 1,
        "color": "string",
        "description": "string",
        "id": 1,
        "name": "Ava Chen",
        "public": true,
        "starred": true,
        "views": 1
      },
      "currentpage": 1,
      "maxpage": 1,
      "nextpage": {},
      "perpage": 1,
      "result": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `collection.clicks` | number |  |
| `collection.color` | string |  |
| `collection.description` | string |  |
| `collection.id` | number |  |
| `collection.name` | string |  |
| `collection.public` | boolean |  |
| `collection.starred` | boolean |  |
| `collection.views` | number |  |
| `currentpage` | number |  |
| `maxpage` | number |  |
| `nextpage` | object |  |
| `perpage` | number |  |
| `result` | number |  |

## Native endpoint

Through the native LinkTwin API, this operation is `GET /collection/:id` (base URL `https://linktw.in/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-collection.md) for the provider-specific parameters and requirements.


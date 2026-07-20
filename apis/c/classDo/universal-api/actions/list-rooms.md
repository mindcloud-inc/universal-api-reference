# ClassDo: List Rooms

Retrieves a list of rooms from ClassDo.

```
GET https://connect.mindcloud.co/v1/universal/classDo/latest/actions/list-rooms
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ClassDo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/classDo/latest/actions/list-rooms?connectionId=$CONNECTION_ID&query=query%20ListRooms%20%7B%20viewer%20%7B%20rooms(input%3A%20%7B%20first%3A%2020%2C%20orderBy%3A%20createdAt_DESC%20%7D)%20%7B%20edges%20%7B%20node%20%7B%20id%20name%20%7D%20%7D%20%7D%20%7D%20%7D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "query ListRooms { viewer { rooms(input: { first: 20, orderBy: createdAt_DESC }) { edges { node { id name } } } } }"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/classDo/latest/actions/list-rooms?${params}`, {
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
| `query` | string | yes | GraphQL query payload for ClassDo. Default: `query ListRooms { viewer { rooms(input: { first: 20, orderBy: createdAt_DESC }) { edges { node { id name } } } } }`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `variables` | object | no | Optional GraphQL variables object. Default: `{}`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "viewer": {
          "rooms": {
            "edges": [
              {
                "node": {
                  "id": "string",
                  "name": "Ava Chen"
                }
              }
            ]
          }
        }
      },
      "errors": [
        {
          "message": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.viewer.rooms.edges[].node.id` | string |  |
| `data.viewer.rooms.edges[].node.name` | string |  |
| `errors[].message` | string |  |

## Native endpoint

Through the native ClassDo API, this operation is `POST /graphql` (base URL `https://api.classdo.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-rooms.md) for the provider-specific parameters and requirements.


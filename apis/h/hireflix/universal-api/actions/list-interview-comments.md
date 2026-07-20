# Hireflix: List Interview Comments

Retrieves comments for an interview in Hireflix.

```
GET https://connect.mindcloud.co/v1/universal/hireflix/latest/actions/list-interview-comments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hireflix `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hireflix/latest/actions/list-interview-comments?connectionId=$CONNECTION_ID&variables.id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "variables.id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hireflix/latest/actions/list-interview-comments?${params}`, {
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
| `variables.id` | string | yes | The Hireflix interview ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "author": {
        "__typename": "Ava Chen",
        "deleted": true,
        "email": "ava@example.com",
        "id": "string",
        "name": "Ava Chen",
        "type": "string"
      },
      "createdAt": 1,
      "id": "string",
      "updatedAt": 1,
      "value": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `author.__typename` | string |  |
| `author.deleted` | boolean |  |
| `author.email` | string |  |
| `author.id` | string |  |
| `author.name` | string |  |
| `author.type` | string |  |
| `createdAt` | number |  |
| `id` | string |  |
| `updatedAt` | number |  |
| `value` | string |  |

## Native endpoint

Through the native Hireflix API, this operation is `POST me` (base URL `https://api.hireflix.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-interview-comments.md) for the provider-specific parameters and requirements.


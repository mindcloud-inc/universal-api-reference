# Moco: List Comments



```
GET https://connect.mindcloud.co/v1/universal/moco/latest/actions/list-comments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Moco `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/moco/latest/actions/list-comments?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/moco/latest/actions/list-comments?${params}`, {
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
| `commentableId` | number | no |  |
| `commentableType` | string | no |  |
| `customProperties` | object | no |  |
| `ids` | string | no |  |
| `manual` | boolean | no |  |
| `updatedAfter` | date | no |  |
| `userId` | number | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "commentableId": 1,
      "commentableType": "string",
      "createdAt": "string",
      "id": 1,
      "manual": true,
      "text": "string",
      "updatedAt": "string",
      "user": {
        "firstname": "Ava",
        "id": 1,
        "lastname": "Chen"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `commentableId` | number |  |
| `commentableType` | string |  |
| `createdAt` | string |  |
| `id` | number |  |
| `manual` | boolean |  |
| `text` | string |  |
| `updatedAt` | string |  |
| `user` | object |  |
| `user.firstname` | string |  |
| `user.id` | number |  |
| `user.lastname` | string |  |

## Native endpoint

Through the native Moco API, this operation is `GET /comments` (base URL `https://{{credentials.domain}}.mocoapp.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-comments.md) for the provider-specific parameters and requirements.


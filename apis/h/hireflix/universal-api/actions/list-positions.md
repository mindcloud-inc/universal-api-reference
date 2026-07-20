# Hireflix: List Positions

Retrieves positions from Hireflix.

```
GET https://connect.mindcloud.co/v1/universal/hireflix/latest/actions/list-positions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hireflix `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hireflix/latest/actions/list-positions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hireflix/latest/actions/list-positions?${params}`, {
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
      "active": true,
      "archived": 1,
      "createdAt": 1,
      "description": "string",
      "expires": 1,
      "id": "string",
      "language": "string",
      "location": "string",
      "name": "Ava Chen",
      "ownerId": "string",
      "public": true,
      "retakes": 1,
      "timeToAnswer": 1,
      "timeToThink": 1,
      "updatedAt": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `archived` | number |  |
| `createdAt` | number |  |
| `description` | string |  |
| `expires` | number |  |
| `id` | string |  |
| `language` | string |  |
| `location` | string |  |
| `name` | string |  |
| `ownerId` | string |  |
| `public` | boolean |  |
| `retakes` | number |  |
| `timeToAnswer` | number |  |
| `timeToThink` | number |  |
| `updatedAt` | number |  |

## Native endpoint

Through the native Hireflix API, this operation is `POST me` (base URL `https://api.hireflix.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-positions.md) for the provider-specific parameters and requirements.


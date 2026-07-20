# DealMachine: List Team Members



```
GET https://connect.mindcloud.co/v1/universal/dealMachine/latest/actions/list-team-members
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DealMachine `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dealMachine/latest/actions/list-team-members?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dealMachine/latest/actions/list-team-members?${params}`, {
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
      "email": "ava@example.com",
      "firstname": "Ava",
      "id": 1,
      "image": "string",
      "lastname": "Chen",
      "name": "Ava Chen",
      "phone": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `email` | string |  |
| `firstname` | string |  |
| `id` | number |  |
| `image` | string |  |
| `lastname` | string |  |
| `name` | string |  |
| `phone` | string |  |

## Native endpoint

Through the native DealMachine API, this operation is `GET /public/v1/team-members/` (base URL `https://api.dealmachine.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-team-members.md) for the provider-specific parameters and requirements.


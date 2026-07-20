# redirect.pizza: List Email Forwards



```
GET https://connect.mindcloud.co/v1/universal/redirectpizza/latest/actions/list-email-forwards
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a redirect.pizza `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/redirectpizza/latest/actions/list-email-forwards?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/redirectpizza/latest/actions/list-email-forwards?${params}`, {
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
      "alias": "string",
      "createdAt": "string",
      "destination": "string",
      "domain": "string",
      "id": 1,
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `alias` | string |  |
| `createdAt` | string |  |
| `destination` | string |  |
| `domain` | string |  |
| `id` | number |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native redirect.pizza API, this operation is `GET /api/v1/email-forwards` (base URL `https://redirect.pizza`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-email-forwards.md) for the provider-specific parameters and requirements.


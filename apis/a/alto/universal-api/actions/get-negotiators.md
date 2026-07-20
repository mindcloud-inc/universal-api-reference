# Alto: Get Negotiators

Retrieves negotiator records from your Alto account.

```
GET https://connect.mindcloud.co/v1/universal/alto/latest/actions/get-negotiators
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Alto `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/alto/latest/actions/get-negotiators?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/alto/latest/actions/get-negotiators?${params}`, {
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
      "authorisedSignatory": true,
      "email": "ava@example.com",
      "id": "string",
      "name": "Ava Chen",
      "phoneNumber": "string",
      "role": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `authorisedSignatory` | boolean |  |
| `email` | string |  |
| `id` | string |  |
| `name` | string |  |
| `phoneNumber` | string |  |
| `role` | string |  |

## Native endpoint

Through the native Alto API, this operation is `GET /negotiators` (base URL `https://api.alto.zoopladev.co.uk`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-negotiators.md) for the provider-specific parameters and requirements.


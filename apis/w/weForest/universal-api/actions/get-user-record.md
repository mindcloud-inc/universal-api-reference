# WeForest: Get user record

Retrieves a user record from WeForest.

```
GET https://connect.mindcloud.co/v1/universal/weForest/latest/actions/get-user-record
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WeForest `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/weForest/latest/actions/get-user-record?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/weForest/latest/actions/get-user-record?${params}`, {
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
| `id` | number | yes | User identifier from WeForest. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "customerId": 1,
      "email": "ava@example.com",
      "firstName": "Ava",
      "id": 1,
      "lastName": "Chen",
      "role": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `customerId` | number |  |
| `email` | string |  |
| `firstName` | string |  |
| `id` | number |  |
| `lastName` | string |  |
| `role` | string |  |

## Native endpoint

Through the native WeForest API, this operation is `GET /users/:id` (base URL `https://api.weforest.org`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user-record.md) for the provider-specific parameters and requirements.


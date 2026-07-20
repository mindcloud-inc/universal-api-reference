# WeForest: Get all projects customer has supported

Retrieves all supported projects for a customer in WeForest.

```
GET https://connect.mindcloud.co/v1/universal/weForest/latest/actions/get-all-projects-customer-has-supported
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WeForest `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/weForest/latest/actions/get-all-projects-customer-has-supported?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/weForest/latest/actions/get-all-projects-customer-has-supported?${params}`, {
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
| `id` | number | yes | Customer identifier from WeForest. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "description": "string",
      "id": 1,
      "imageUrl": "https://example.com",
      "name": "Ava Chen",
      "price": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string |  |
| `id` | number |  |
| `imageUrl` | string |  |
| `name` | string |  |
| `price` | number |  |

## Native endpoint

Through the native WeForest API, this operation is `GET /customers/:id/projects` (base URL `https://api.weforest.org`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-all-projects-customer-has-supported.md) for the provider-specific parameters and requirements.


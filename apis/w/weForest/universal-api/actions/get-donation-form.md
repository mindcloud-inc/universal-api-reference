# WeForest: Get donation form

Retrieves a donation form from WeForest.

```
GET https://connect.mindcloud.co/v1/universal/weForest/latest/actions/get-donation-form
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WeForest `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/weForest/latest/actions/get-donation-form?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/weForest/latest/actions/get-donation-form?${params}`, {
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
| `id` | number | yes | Donation form identifier from WeForest. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "customerId": 1,
      "description": "string",
      "id": 1,
      "products": {},
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `customerId` | number |  |
| `description` | string |  |
| `id` | number |  |
| `products` | object |  |
| `title` | string |  |

## Native endpoint

Through the native WeForest API, this operation is `GET /forms/:id` (base URL `https://api.weforest.org`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-donation-form.md) for the provider-specific parameters and requirements.


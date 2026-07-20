# Shippify: Break Route

Deletes routes in Shippify and returns deliveries to processing.

```
DELETE https://connect.mindcloud.co/v1/universal/shippify/latest/actions/break-route
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Shippify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/shippify/latest/actions/break-route?connectionId=$CONNECTION_ID&routes%5B%5D=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "routes[]": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/shippify/latest/actions/break-route?${params}`, {
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
| `routes[]` | array<string> | yes | Required array of route identifiers to break. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": "string",
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | string | Shippify result code. |
| `message` | string | Shippify result message. |

## Native endpoint

Through the native Shippify API, this operation is `PUT /v1/routes/destroy` (base URL `https://api.shippify.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/break-route.md) for the provider-specific parameters and requirements.


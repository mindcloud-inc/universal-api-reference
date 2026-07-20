# Shippify: Change Route Status

Updates a route status in Shippify.

```
PUT https://connect.mindcloud.co/v1/universal/shippify/latest/actions/change-route-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Shippify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/shippify/latest/actions/change-route-status" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "status": "string",
  "comment": "string",
  "author": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/shippify/latest/actions/change-route-status', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "status": "string",
    "comment": "string",
    "author": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Identifier of the route whose status should change. |
| `status` | string | yes | New Shippify route status. |
| `comment` | string | yes | Comment explaining the route status change. |
| `author` | object | yes | Required object describing the operator or actor making the route status change. |
| `reasonByCompany[]` | array<object> | no | Optional array of predefined company reasons for the route status change. |

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

Through the native Shippify API, this operation is `PATCH /v1/routes/:id/status` (base URL `https://api.shippify.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/change-route-status.md) for the provider-specific parameters and requirements.


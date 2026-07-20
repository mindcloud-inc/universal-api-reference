# EasyPost: Create And Verify Address

Creates and verifies a new address in EasyPost.

```
POST https://connect.mindcloud.co/v1/universal/easyPost/latest/actions/create-and-verify-address
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EasyPost `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/easyPost/latest/actions/create-and-verify-address" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "address": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/easyPost/latest/actions/create-and-verify-address', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "address": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `address` | object | yes | Address object to create and verify. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `verify[]` | array<string> | no | Optional verification types to request, such as delivery. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "city": "string",
      "country": "string",
      "id": "string",
      "mode": "string",
      "name": "Ava Chen",
      "object": "string",
      "state": "string",
      "street1": "string",
      "verifications": {},
      "zip": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `city` | string |  |
| `country` | string |  |
| `id` | string |  |
| `mode` | string |  |
| `name` | string |  |
| `object` | string |  |
| `state` | string |  |
| `street1` | string |  |
| `verifications` | object |  |
| `zip` | string |  |

## Native endpoint

Through the native EasyPost API, this operation is `POST /addresses/create_and_verify` (base URL `https://api.easypost.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-and-verify-address.md) for the provider-specific parameters and requirements.


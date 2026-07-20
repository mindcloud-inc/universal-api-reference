# Copperx: Get Withdrawal Address

Retrieves a withdrawal address from Copperx.

```
GET https://connect.mindcloud.co/v1/universal/copperx/latest/actions/get-withdrawal-address
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Copperx `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/copperx/latest/actions/get-withdrawal-address?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/copperx/latest/actions/get-withdrawal-address?${params}`, {
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
| `id` | string | yes | Withdrawal address ID path parameter. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address": "string",
      "chainId": 1,
      "createdAt": "string",
      "id": "string",
      "isDefault": true,
      "name": "Ava Chen",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address` | string |  |
| `chainId` | number |  |
| `createdAt` | string |  |
| `id` | string |  |
| `isDefault` | boolean |  |
| `name` | string |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native Copperx API, this operation is `GET /organization/withdrawal-addresses/{id}` (base URL `https://api.copperx.dev/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-withdrawal-address.md) for the provider-specific parameters and requirements.


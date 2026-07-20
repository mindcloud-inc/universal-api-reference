# Voucherify: Get Export

Retrieves an export from Voucherify.

```
GET https://connect.mindcloud.co/v1/universal/voucherify/latest/actions/get-export
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Voucherify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/voucherify/latest/actions/get-export?connectionId=$CONNECTION_ID&exportId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "exportId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/voucherify/latest/actions/get-export?${params}`, {
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
| `exportId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "channel": "string",
      "createdAt": "string",
      "exportedObject": "string",
      "id": "string",
      "keyId": "string",
      "object": "string",
      "parameters": {},
      "result": {},
      "status": "string",
      "userId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `channel` | string |  |
| `createdAt` | string |  |
| `exportedObject` | string |  |
| `id` | string |  |
| `keyId` | string |  |
| `object` | string |  |
| `parameters` | object |  |
| `result` | object |  |
| `status` | string |  |
| `userId` | string |  |

## Native endpoint

Through the native Voucherify API, this operation is `GET /exports/:exportId` (base URL `https://us1.api.voucherify.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-export.md) for the provider-specific parameters and requirements.


# Lightfunnels: Get Customer



```
GET https://connect.mindcloud.co/v1/universal/lightfunnels/latest/actions/get-customer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lightfunnels `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lightfunnels/latest/actions/get-customer?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lightfunnels/latest/actions/get-customer?${params}`, {
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
      "node": {
        "createdAt": "string",
        "email": "ava@example.com",
        "fullName": "Ava Chen",
        "id": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `node` | object | Customer node. |
| `node.createdAt` | string | Creation timestamp. |
| `node.email` | string | Customer email. |
| `node.fullName` | string | Customer full name. |
| `node.id` | string | Customer id. |

## Native endpoint

Through the native Lightfunnels API, this operation is `POST /api/v2` (base URL `https://services.lightfunnels.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-customer.md) for the provider-specific parameters and requirements.


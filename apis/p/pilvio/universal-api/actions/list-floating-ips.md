# Pilvio: List Floating IPs



```
GET https://connect.mindcloud.co/v1/universal/pilvio/latest/actions/list-floating-ips
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pilvio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pilvio/latest/actions/list-floating-ips?connectionId=$CONNECTION_ID&billingAccountId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "billingAccountId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pilvio/latest/actions/list-floating-ips?${params}`, {
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
| `billingAccountId` | string | yes | Billing account ID used to filter floating IPs. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address": "string",
      "billingAccountId": 1,
      "id": 1,
      "type": "string",
      "userId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address` | string |  |
| `billingAccountId` | number |  |
| `id` | number |  |
| `type` | string |  |
| `userId` | number |  |

## Native endpoint

Through the native Pilvio API, this operation is `GET /network/ip_addresses` (base URL `https://api.pilvio.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-floating-ips.md) for the provider-specific parameters and requirements.


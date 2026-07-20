# GoAffPro: List Affiliate Customer Connections

Retrieves affiliate customer connections from GoAffPro.

```
GET https://connect.mindcloud.co/v1/universal/goAffPro/latest/actions/list-affiliate-customer-connections
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GoAffPro `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/goAffPro/latest/actions/list-affiliate-customer-connections?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/goAffPro/latest/actions/list-affiliate-customer-connections?${params}`, {
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
| `affiliateId` | string | no | Only return connections for this affiliate ID. |
| `customerEmail` | string | no | Only return connections for this customer email address. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "affiliate": {
        "id": 1
      },
      "createdAt": "string",
      "customer": {
        "email": "ava@example.com",
        "name": "Ava Chen"
      },
      "id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `affiliate.id` | number |  |
| `createdAt` | string |  |
| `customer.email` | string |  |
| `customer.name` | string |  |
| `id` | number |  |

## Native endpoint

Through the native GoAffPro API, this operation is `GET /admin/connections` (base URL `https://api.goaffpro.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-affiliate-customer-connections.md) for the provider-specific parameters and requirements.


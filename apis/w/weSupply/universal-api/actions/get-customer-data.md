# WeSupply: Get Customer Data

Retrieves customer data from WeSupply.

```
GET https://connect.mindcloud.co/v1/universal/weSupply/latest/actions/get-customer-data
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WeSupply `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/weSupply/latest/actions/get-customer-data?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/weSupply/latest/actions/get-customer-data?${params}`, {
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
| `customerEmail` | string | no | The customer email address whose data should be retrieved. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "CustomerEmail": "ava@example.com",
      "OrderContact": "string",
      "OrderExternalOrderID": "string",
      "OrderNumber": "string",
      "OrderShippingPhone": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `CustomerEmail` | string |  |
| `OrderContact` | string |  |
| `OrderExternalOrderID` | string |  |
| `OrderNumber` | string |  |
| `OrderShippingPhone` | string |  |

## Native endpoint

Through the native WeSupply API, this operation is `GET /gdpr/get` (base URL `https://{{credentials.subdomain}}.labs.wesupply.xyz/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-customer-data.md) for the provider-specific parameters and requirements.


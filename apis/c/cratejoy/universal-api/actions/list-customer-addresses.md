# Cratejoy: List Customer Addresses

Retrieves a customer's addresses from Cratejoy.

```
GET https://connect.mindcloud.co/v1/universal/cratejoy/latest/actions/list-customer-addresses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cratejoy `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cratejoy/latest/actions/list-customer-addresses?connectionId=$CONNECTION_ID&limit=25&offset=0&customerId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "customerId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cratejoy/latest/actions/list-customer-addresses?${params}`, {
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
| `customerId` | number | yes | The Cratejoy customer ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "city": "string",
      "country": "string",
      "id": 1,
      "state": "string",
      "status": 1,
      "status_message": "string",
      "street": "string",
      "to": "string",
      "url": "https://example.com",
      "zip_code": "string"
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
| `id` | number |  |
| `state` | string |  |
| `status` | number |  |
| `status_message` | string |  |
| `street` | string |  |
| `to` | string |  |
| `url` | string |  |
| `zip_code` | string |  |

## Native endpoint

Through the native Cratejoy API, this operation is `GET /v1/customers/:customerId/addresses/` (base URL `https://api.cratejoy.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-customer-addresses.md) for the provider-specific parameters and requirements.


# Yampi: Get Customer Address

Retrieves the specified customer address from Yampi.

```
GET https://connect.mindcloud.co/v1/universal/yampi/latest/actions/get-customer-address
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Yampi `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/yampi/latest/actions/get-customer-address?connectionId=$CONNECTION_ID&customerId=string&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "customerId": "string",
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/yampi/latest/actions/get-customer-address?${params}`, {
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
| `customerId` | string | yes |  |
| `id` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "city": "string",
      "id": 1,
      "state": "string",
      "street": "string",
      "zipcode": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `city` | string |  |
| `id` | number |  |
| `state` | string |  |
| `street` | string |  |
| `zipcode` | string |  |

## Native endpoint

Through the native Yampi API, this operation is `GET /:merchantAlias/customers/:customerId/addresses/:id` (base URL `https://api.dooki.com.br/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-customer-address.md) for the provider-specific parameters and requirements.


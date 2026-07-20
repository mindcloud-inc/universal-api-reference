# Customer.io: List Customers, Attributes, and Devices

Retrieves customers, attributes, and devices from Customer.io by ID.

```
GET https://connect.mindcloud.co/v1/universal/customerio/latest/actions/list-customers-attributes-and-devices
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Customer.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/customerio/latest/actions/list-customers-attributes-and-devices?connectionId=$CONNECTION_ID&ids%5B%5D=mc_local_play_20260306" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "ids[]": "mc_local_play_20260306"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/customerio/latest/actions/list-customers-attributes-and-devices?${params}`, {
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
| `ids[]` | array<string> | yes | An array of 1 to 100 customer IDs. Example: `mc_local_play_20260306`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {},
      "devices": [
        {}
      ],
      "id": "string",
      "identifiers": {},
      "timestamps": {},
      "unsubscribed": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attributes` | object | The customer attributes object. |
| `devices` | array<object> | Devices associated with the customer. |
| `id` | string | The customer identifier. |
| `identifiers` | object | The customer identifier map returned by Customer.io. |
| `timestamps` | object | Attribute update timestamps keyed by field. |
| `unsubscribed` | boolean | Whether the customer is globally unsubscribed. |

## Native endpoint

Through the native Customer.io API, this operation is `POST /v1/customers/attributes` (base URL `https://api.customer.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-customers-attributes-and-devices.md) for the provider-specific parameters and requirements.


# Invoice Ninja: Update Tax Data



```
PUT https://connect.mindcloud.co/v1/universal/invoiceNinja/latest/actions/update-tax-data
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Invoice Ninja `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/invoiceNinja/latest/actions/update-tax-data" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "clientId": "string",
  "address1": "123 New Street",
  "city": "New York",
  "state": "NY",
  "postalCode": "10001",
  "countryId": "840"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/invoiceNinja/latest/actions/update-tax-data', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "clientId": "string",
    "address1": "123 New Street",
    "city": "New York",
    "state": "NY",
    "postalCode": "10001",
    "countryId": "840"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `clientId` | string | yes | Hashed client ID. |
| `address1` | string | yes | Street address used to refresh the client's tax data. Example: `123 New Street`. |
| `city` | string | yes | City used to refresh the client's tax data. Example: `New York`. |
| `state` | string | yes | State or region used to refresh the client's tax data. Example: `NY`. |
| `postalCode` | string | yes | Postal code used to refresh the client's tax data. Example: `10001`. |
| `countryId` | number | yes | Country identifier used to refresh the client's tax data. Example: `840`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address1": "string",
      "balance": 1,
      "city": "string",
      "contacts": [
        {}
      ],
      "country_id": "string",
      "display_name": "Ava Chen",
      "id": "string",
      "name": "Ava Chen",
      "number": "string",
      "postal_code": "string",
      "settings": {},
      "state": "string",
      "tax_info": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address1` | string | Primary street address on the returned client record. |
| `balance` | number | Outstanding balance for the client. |
| `city` | string | City on the returned client record. |
| `contacts` | array<object> | Client contact records returned by Invoice Ninja. |
| `country_id` | string | Country identifier. |
| `display_name` | string | Display label for the client. |
| `id` | string | Hashed client ID. |
| `name` | string | Client company or organization name. |
| `number` | string | Client number. |
| `postal_code` | string | Postal code on the returned client record. |
| `settings` | object | Client-level settings object. |
| `state` | string | State or region on the returned client record. |
| `tax_info` | object | Tax information object returned after the refresh. |

## Native endpoint

Through the native Invoice Ninja API, this operation is `POST /clients/:client/updateTaxData` (base URL `https://invoicing.co/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-tax-data.md) for the provider-specific parameters and requirements.


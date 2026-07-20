# Atera: Update customer

Updates an existing customer in Atera.

```
PUT https://connect.mindcloud.co/v1/universal/atera/latest/actions/update-customer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Atera `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/atera/latest/actions/update-customer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "customerId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/atera/latest/actions/update-customer', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "customerId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `address` | string | no | Street address. |
| `businessNumber` | string | no | Business number. |
| `city` | string | no | City. |
| `country` | string | no | Country. |
| `customerId` | number | yes | System customer ID. |
| `customerName` | string | no | Customer name. |
| `domain` | string | no | Customer domain. |
| `fax` | string | no | Fax number. |
| `latitude` | number | no | Latitude. |
| `links` | string | no | Related links. |
| `longitude` | number | no | Longitude. |
| `notes` | string | no | Customer notes. |
| `phone` | string | no | Phone number. |
| `state` | string | no | State or region. |
| `zipCodeStr` | string | no | ZIP or postal code. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ActionID": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ActionID` | string |  |

## Native endpoint

Through the native Atera API, this operation is `PUT /api/v3/customers/:customerId` (base URL `https://app.atera.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-customer.md) for the provider-specific parameters and requirements.


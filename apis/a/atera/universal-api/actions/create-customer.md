# Atera: Create customer

Creates a customer in Atera.

```
POST https://connect.mindcloud.co/v1/universal/atera/latest/actions/create-customer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Atera `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/atera/latest/actions/create-customer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "customerName": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/atera/latest/actions/create-customer', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "customerName": "Ava Chen"
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
| `createdOn` | string | no | Customer creation timestamp. |
| `customerName` | string | yes | Customer name. |
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

Through the native Atera API, this operation is `POST /api/v3/customers` (base URL `https://app.atera.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-customer.md) for the provider-specific parameters and requirements.


# Digistore24: Update Buyer

Updates an existing buyer in Digistore24.

```
PUT https://connect.mindcloud.co/v1/universal/digistore24/latest/actions/update-buyer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Digistore24 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/digistore24/latest/actions/update-buyer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "buyerId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/digistore24/latest/actions/update-buyer', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "buyerId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `buyerId` | number | yes | Buyer ID |
| `email` | string | no | Buyer email address |
| `firstName` | string | no | Buyer first name |
| `lastName` | string | no | Buyer last name |
| `salutation` | string | no | Buyer salutation |
| `title` | string | no | Buyer title |
| `company` | string | no | Buyer company |
| `streetName` | string | no | Street name |
| `streetNumber` | string | no | Street number |
| `phoneNumber` | string | no | Phone number |
| `city` | string | no | City |
| `zipcode` | string | no | ZIP or postal code |
| `state` | string | no | State or province |
| `country` | string | no | ISO country code |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Digistore24 API returns.

## Native endpoint

Through the native Digistore24 API, this operation is `PUT /updateBuyer` (base URL `https://www.digistore24.com/api/call`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-buyer.md) for the provider-specific parameters and requirements.


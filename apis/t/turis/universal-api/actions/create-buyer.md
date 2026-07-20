# Turis: Create Buyer

Creates a new buyer in Turis.

```
POST https://connect.mindcloud.co/v1/universal/turis/latest/actions/create-buyer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Turis `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/turis/latest/actions/create-buyer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "company_id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/turis/latest/actions/create-buyer', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "company_id": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `address` | string | no | Buyer street address. |
| `company_id` | number | yes | Company ID the buyer belongs to. |
| `email` | string | no | Buyer email address. |
| `first_name` | string | no | Buyer first name. |
| `invite_buyer` | boolean | no | Whether to send a buyer invite. |
| `language_id` | number | no | Buyer language identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address": "string",
      "city": "string",
      "companyId": 1,
      "country": "string",
      "discount": "string",
      "email": "ava@example.com",
      "id": 1,
      "name": "Ava Chen",
      "phoneNumber": "string",
      "zipCode": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address` | string |  |
| `city` | string |  |
| `companyId` | number |  |
| `country` | string |  |
| `discount` | string |  |
| `email` | string |  |
| `id` | number |  |
| `name` | string |  |
| `phoneNumber` | string |  |
| `zipCode` | string |  |

## Native endpoint

Through the native Turis API, this operation is `POST /api/public/v1/buyers` (base URL `https://{{credentials.tenant}}.turis.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-buyer.md) for the provider-specific parameters and requirements.


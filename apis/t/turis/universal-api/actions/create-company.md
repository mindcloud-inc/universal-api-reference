# Turis: Create Company

Creates a new company in Turis.

```
POST https://connect.mindcloud.co/v1/universal/turis/latest/actions/create-company
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Turis `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/turis/latest/actions/create-company" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "currency_id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/turis/latest/actions/create-company', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "currency_id": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `address` | string | no | Company street address. |
| `allow_users` | string | no | Whether buyers can be created for the company. |
| `city` | string | no | Company city. |
| `company_name` | string | no | Company name in Turis. |
| `company_reg_no` | string | no | Company registration number. |
| `company_slug` | string | no | Unique slug for the company. |
| `country_iso_code` | string | no | Two-letter country code for the company. |
| `currency_id` | number | yes | Currency identifier for the company. |
| `customer_no` | string | no | Customer number for the company. |
| `discount` | string | no | Company discount percentage. |
| `email` | string | no | Company email address. |
| `free_shipping_limit` | string | no | Free shipping threshold. |
| `language_id` | string | no | Company language identifier. |
| `order_confirmation_email` | string | no | Email for order confirmations. |
| `phone_number` | string | no | Company phone number. |
| `tz` | string | no | Company time zone. |
| `vat_number` | string | no | Company VAT number. |
| `website` | string | no | Company website. |
| `zip_code` | string | no | Company ZIP or postal code. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address": "string",
      "companySlug": "string",
      "currencyId": 1,
      "discount": 1,
      "forwarderName": "Ava Chen",
      "id": 1,
      "name": "Ava Chen",
      "specialPriceLists": [
        {
          "id": 1
        }
      ],
      "vatTypeId": 1,
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
| `companySlug` | string |  |
| `currencyId` | number |  |
| `discount` | number |  |
| `forwarderName` | string |  |
| `id` | number |  |
| `name` | string |  |
| `specialPriceLists[].id` | number |  |
| `vatTypeId` | number |  |
| `zipCode` | string |  |

## Native endpoint

Through the native Turis API, this operation is `POST /api/public/v1/companies` (base URL `https://{{credentials.tenant}}.turis.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-company.md) for the provider-specific parameters and requirements.


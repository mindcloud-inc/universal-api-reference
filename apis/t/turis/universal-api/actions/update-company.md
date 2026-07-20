# Turis: Update Company

Updates an existing company in Turis.

```
PUT https://connect.mindcloud.co/v1/universal/turis/latest/actions/update-company
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Turis `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/turis/latest/actions/update-company" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/turis/latest/actions/update-company', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "address": "string",
      "companySlug": "string",
      "currencyId": 1,
      "discount": "string",
      "forwarderName": "Ava Chen",
      "id": 1,
      "name": "Ava Chen",
      "orderConfirmationEmail": "ava@example.com",
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
| `discount` | string |  |
| `forwarderName` | string |  |
| `id` | number |  |
| `name` | string |  |
| `orderConfirmationEmail` | string |  |
| `vatTypeId` | number |  |
| `zipCode` | string |  |

## Native endpoint

Through the native Turis API, this operation is `PUT /api/public/v1/companies/:companyId` (base URL `https://{{credentials.tenant}}.turis.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-company.md) for the provider-specific parameters and requirements.


# Turis: List Companies

Retrieves companies from Turis.

```
GET https://connect.mindcloud.co/v1/universal/turis/latest/actions/list-companies
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Turis `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/turis/latest/actions/list-companies?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/turis/latest/actions/list-companies?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
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

Through the native Turis API, this operation is `GET /api/public/v1/companies` (base URL `https://{{credentials.tenant}}.turis.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-companies.md) for the provider-specific parameters and requirements.


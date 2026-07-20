# Turis: List Buyers

Retrieves buyers from Turis.

```
GET https://connect.mindcloud.co/v1/universal/turis/latest/actions/list-buyers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Turis `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/turis/latest/actions/list-buyers?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/turis/latest/actions/list-buyers?${params}`, {
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

Through the native Turis API, this operation is `GET /api/public/v1/buyers` (base URL `https://{{credentials.tenant}}.turis.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-buyers.md) for the provider-specific parameters and requirements.


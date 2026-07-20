# Turis: List Deliveries

Retrieves deliveries from Turis.

```
GET https://connect.mindcloud.co/v1/universal/turis/latest/actions/list-deliveries
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Turis `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/turis/latest/actions/list-deliveries?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/turis/latest/actions/list-deliveries?${params}`, {
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
      "companyName": "Ava Chen",
      "country": "string",
      "firstName": "Ava",
      "id": 1,
      "lastName": "Chen",
      "locationName": "Ava Chen",
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
| `companyName` | string |  |
| `country` | string |  |
| `firstName` | string |  |
| `id` | number |  |
| `lastName` | string |  |
| `locationName` | string |  |
| `zipCode` | string |  |

## Native endpoint

Through the native Turis API, this operation is `GET /api/public/v1/deliveries` (base URL `https://{{credentials.tenant}}.turis.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-deliveries.md) for the provider-specific parameters and requirements.


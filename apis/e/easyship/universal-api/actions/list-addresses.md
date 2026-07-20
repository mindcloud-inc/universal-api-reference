# Easyship: List Addresses

Retrieves a list of addresses from Easyship.

```
GET https://connect.mindcloud.co/v1/universal/easyship/latest/actions/list-addresses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Easyship `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/easyship/latest/actions/list-addresses?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/easyship/latest/actions/list-addresses?${params}`, {
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
      "city": "string",
      "companyName": "Ava Chen",
      "contactEmail": "ava@example.com",
      "contactName": "Ava Chen",
      "contactPhone": "string",
      "countryAlpha2": "string",
      "defaultFor": {
        "billing": true,
        "pickup": true,
        "return": true,
        "sender": true
      },
      "id": "string",
      "line1": "string",
      "line2": "string",
      "postalCode": "string",
      "state": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `city` | string |  |
| `companyName` | string |  |
| `contactEmail` | string |  |
| `contactName` | string |  |
| `contactPhone` | string |  |
| `countryAlpha2` | string |  |
| `defaultFor` | object |  |
| `defaultFor.billing` | boolean |  |
| `defaultFor.pickup` | boolean |  |
| `defaultFor.return` | boolean |  |
| `defaultFor.sender` | boolean |  |
| `id` | string |  |
| `line1` | string |  |
| `line2` | string |  |
| `postalCode` | string |  |
| `state` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Easyship API, this operation is `GET /addresses` (base URL `https://public-api.easyship.com/2024-09`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-addresses.md) for the provider-specific parameters and requirements.


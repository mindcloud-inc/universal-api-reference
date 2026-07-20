# Bookvault: List Addresses

Retrieves saved addresses from your Bookvault account.

```
GET https://connect.mindcloud.co/v1/universal/bookvault/latest/actions/list-addresses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bookvault `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bookvault/latest/actions/list-addresses?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bookvault/latest/actions/list-addresses?${params}`, {
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
      "Address1": "string",
      "Addressee": "string",
      "CommonAddrID": 1,
      "Company": "string",
      "Country": {},
      "Email": "ava@example.com",
      "Postcode": "string",
      "Town": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Address1` | string |  |
| `Addressee` | string |  |
| `CommonAddrID` | number |  |
| `Company` | string |  |
| `Country` | object |  |
| `Email` | string |  |
| `Postcode` | string |  |
| `Town` | string |  |

## Native endpoint

Through the native Bookvault API, this operation is `GET /Addresses` (base URL `https://api.bookvault.app/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-addresses.md) for the provider-specific parameters and requirements.


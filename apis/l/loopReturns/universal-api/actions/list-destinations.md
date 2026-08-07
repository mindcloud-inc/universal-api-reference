# Loop Returns: List Destinations

Retrieve all destinations.

```
GET https://connect.mindcloud.co/v1/universal/loopReturns/latest/actions/list-destinations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Loop Returns `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/loopReturns/latest/actions/list-destinations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/loopReturns/latest/actions/list-destinations?${params}`, {
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
      "address": {
        "address1": "string",
        "address2": "string",
        "city": "string",
        "company": "string",
        "country": "string",
        "countryCode": "string",
        "name": "Ava Chen",
        "state": "string",
        "zip": "string"
      },
      "enabled": true,
      "id": 1,
      "name": "Ava Chen",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address.address1` | string |  |
| `address.address2` | string |  |
| `address.city` | string |  |
| `address.company` | string |  |
| `address.country` | string |  |
| `address.countryCode` | string |  |
| `address.name` | string |  |
| `address.state` | string |  |
| `address.zip` | string |  |
| `enabled` | boolean |  |
| `id` | number |  |
| `name` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Loop Returns API, this operation is `GET /destinations` (base URL `https://api.loopreturns.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-destinations.md) for the provider-specific parameters and requirements.


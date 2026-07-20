# Bolna: Search Phone Numbers

Finds available phone numbers by region, locality, or pattern.

```
GET https://connect.mindcloud.co/v1/universal/bolna/latest/actions/search-phone-numbers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bolna `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bolna/latest/actions/search-phone-numbers?connectionId=$CONNECTION_ID&country=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "country": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bolna/latest/actions/search-phone-numbers?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `country` | string | yes | Country code for the phone-number search, such as US or IN. |
| `pattern` | string | no | Three-character prefix to search against the phone number. |
| `provider` | string | no | Telephony provider filter for the search result. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "friendlyName": "Ava Chen",
      "locality": "string",
      "phoneNumber": "string",
      "price": 1,
      "provider": "string",
      "region": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `friendlyName` | string |  |
| `locality` | string |  |
| `phoneNumber` | string |  |
| `price` | number |  |
| `provider` | string |  |
| `region` | string |  |

## Native endpoint

Through the native Bolna API, this operation is `GET /phone-numbers/search` (base URL `https://api.bolna.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-phone-numbers.md) for the provider-specific parameters and requirements.


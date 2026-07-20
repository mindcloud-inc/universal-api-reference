# Evenium: List Hotels

Retrieves hotels from Evenium.

```
GET https://connect.mindcloud.co/v1/universal/evenium/latest/actions/list-hotels
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Evenium `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/evenium/latest/actions/list-hotels?connectionId=$CONNECTION_ID&eventId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "eventId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/evenium/latest/actions/list-hotels?${params}`, {
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
| `eventId` | number | yes | The Evenium event ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "adminInfo": "string",
      "disabledAccess": true,
      "email": "ava@example.com",
      "fax": "string",
      "group": "string",
      "id": 1,
      "location": {},
      "name": "Ava Chen",
      "parking": true,
      "phone": "string",
      "rooms": [
        {}
      ],
      "smoking": true,
      "stars": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `adminInfo` | string | Additional administrative information. |
| `disabledAccess` | boolean | Whether disabled access is available. |
| `email` | string | Hotel email address. |
| `fax` | string | Hotel fax number. |
| `group` | string | Hotel group label. |
| `id` | number | Hotel ID. |
| `location` | object | Hotel location object. |
| `name` | string | Hotel name. |
| `parking` | boolean | Whether parking is available. |
| `phone` | string | Hotel phone number. |
| `rooms` | array<object> | Hotel rooms. |
| `smoking` | boolean | Whether smoking is allowed. |
| `stars` | number | Hotel star rating. |

## Native endpoint

Through the native Evenium API, this operation is `GET /events/:eventId/hotels` (base URL `https://evenium.com/api/1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-hotels.md) for the provider-specific parameters and requirements.


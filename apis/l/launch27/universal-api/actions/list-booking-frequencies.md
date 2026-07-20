# Launch27: List Booking Frequencies

Retrieves booking frequencies from Launch27.

```
GET https://connect.mindcloud.co/v1/universal/launch27/latest/actions/list-booking-frequencies
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Launch27 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/launch27/latest/actions/list-booking-frequencies?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/launch27/latest/actions/list-booking-frequencies?${params}`, {
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
      "amount": 1,
      "default": true,
      "exclude_first": true,
      "id": 1,
      "interval": "string",
      "name": "Ava Chen",
      "percent": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | number |  |
| `default` | boolean |  |
| `exclude_first` | boolean |  |
| `id` | number |  |
| `interval` | string |  |
| `name` | string |  |
| `percent` | number |  |

## Native endpoint

Through the native Launch27 API, this operation is `GET booking/frequencies` (base URL `https://{{credentials.subdomain}}.launch27.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-booking-frequencies.md) for the provider-specific parameters and requirements.


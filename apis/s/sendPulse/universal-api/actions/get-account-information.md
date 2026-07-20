# SendPulse: Get Account Information

Retrieves account profile information from SendPulse.

```
GET https://connect.mindcloud.co/v1/universal/sendPulse/latest/actions/get-account-information
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SendPulse `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sendPulse/latest/actions/get-account-information?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sendPulse/latest/actions/get-account-information?${params}`, {
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
      "avatar": "string",
      "city": "string",
      "country": "string",
      "currency": "string",
      "email": "ava@example.com",
      "first_name": "Ava",
      "id": 1,
      "lang": "string",
      "last_name": "Chen",
      "locale": "string",
      "name": "Ava Chen",
      "phone": "string",
      "phone_confirm": true,
      "time_zone": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `avatar` | string |  |
| `city` | string |  |
| `country` | string |  |
| `currency` | string |  |
| `email` | string |  |
| `first_name` | string |  |
| `id` | number |  |
| `lang` | string |  |
| `last_name` | string |  |
| `locale` | string |  |
| `name` | string |  |
| `phone` | string |  |
| `phone_confirm` | boolean |  |
| `time_zone` | string |  |

## Native endpoint

Through the native SendPulse API, this operation is `GET /user/info` (base URL `https://api.sendpulse.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-account-information.md) for the provider-specific parameters and requirements.


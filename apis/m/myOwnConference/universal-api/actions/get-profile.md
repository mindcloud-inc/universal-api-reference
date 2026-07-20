# MyOwnConference: Get profile

Retrieves the current MyOwnConference account profile.

```
GET https://connect.mindcloud.co/v1/universal/myOwnConference/latest/actions/get-profile
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MyOwnConference `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/myOwnConference/latest/actions/get-profile?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/myOwnConference/latest/actions/get-profile?${params}`, {
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
      "company": "string",
      "email": "ava@example.com",
      "gateway": "string",
      "language": "string",
      "name": "Ava Chen",
      "subscribe": "string",
      "timemove": "string",
      "timezone": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `company` | string | Company name or billing entity. |
| `email` | string | Account email address. |
| `gateway` | string | Configured payment gateway. |
| `language` | string | Default account language. |
| `name` | string | Profile display name. |
| `subscribe` | string | News subscription flag. |
| `timemove` | string | Daylight saving handling flag. |
| `timezone` | number | Timezone offset in minutes. |

## Native endpoint

Through the native MyOwnConference API, this operation is `POST /` (base URL `https://api.mywebinar.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-profile.md) for the provider-specific parameters and requirements.


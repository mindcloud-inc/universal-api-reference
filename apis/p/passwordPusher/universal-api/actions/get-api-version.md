# Password Pusher: Get API Version

Retrieves API version and feature details from Password Pusher.

```
GET https://connect.mindcloud.co/v1/universal/passwordPusher/latest/actions/get-api-version
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Password Pusher `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/passwordPusher/latest/actions/get-api-version?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/passwordPusher/latest/actions/get-api-version?${params}`, {
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
      "api_version": "string",
      "application_version": "string",
      "edition": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `api_version` | string |  |
| `application_version` | string |  |
| `edition` | string |  |

## Native endpoint

Through the native Password Pusher API, this operation is `GET /version` (base URL `https://eu.pwpush.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-api-version.md) for the provider-specific parameters and requirements.


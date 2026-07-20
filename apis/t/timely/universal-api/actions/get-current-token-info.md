# Timely: Get Current Token Info

Retrieves details about the current OAuth access token from Timely.

```
GET https://connect.mindcloud.co/v1/universal/timely/latest/actions/get-current-token-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Timely `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/timely/latest/actions/get-current-token-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/timely/latest/actions/get-current-token-info?${params}`, {
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
      "application": {
        "name": "Ava Chen",
        "uid": "string"
      },
      "expires_in": 1,
      "resource_owner_id": 1,
      "scope": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `application` | object |  |
| `application.name` | string |  |
| `application.uid` | string |  |
| `expires_in` | number |  |
| `resource_owner_id` | number |  |
| `scope` | array<string> |  |

## Native endpoint

Through the native Timely API, this operation is `GET /1.1/oauth/token/info` (base URL `https://api.timelyapp.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-current-token-info.md) for the provider-specific parameters and requirements.


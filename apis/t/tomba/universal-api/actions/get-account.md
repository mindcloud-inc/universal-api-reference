# Tomba: Get Account

Retrieves the current account from Tomba.

```
GET https://connect.mindcloud.co/v1/universal/tomba/latest/actions/get-account
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tomba `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tomba/latest/actions/get-account?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tomba/latest/actions/get-account?${params}`, {
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
      "confirmed": true,
      "country": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "first_name": "Ava",
      "image": "string",
      "last_name": "Chen",
      "pricing": {
        "available_searches": 1
      },
      "requests": {
        "domains": {
          "available": 1
        }
      },
      "user_id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `confirmed` | boolean |  |
| `country` | string |  |
| `created_at` | date |  |
| `email` | string |  |
| `first_name` | string |  |
| `image` | string |  |
| `last_name` | string |  |
| `pricing.available_searches` | number |  |
| `requests.domains.available` | number |  |
| `user_id` | number |  |

## Native endpoint

Through the native Tomba API, this operation is `GET /me` (base URL `https://api.tomba.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-account.md) for the provider-specific parameters and requirements.


# Boomlify: Get Account Info

Retrieves account information from Boomlify.

```
GET https://connect.mindcloud.co/v1/universal/boomlify/latest/actions/get-account-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Boomlify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/boomlify/latest/actions/get-account-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/boomlify/latest/actions/get-account-info?${params}`, {
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
      "account": {
        "api_key_prefix": "string",
        "credits_balance": 1,
        "email": "ava@example.com",
        "member_since": "2026-05-07T12:00:00.000Z",
        "tier": "string",
        "user_id": "string"
      },
      "features": {},
      "meta": {
        "request_time": "2026-05-07T12:00:00.000Z"
      },
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `account` | object |  |
| `account.api_key_prefix` | string |  |
| `account.credits_balance` | number |  |
| `account.email` | string |  |
| `account.member_since` | date |  |
| `account.tier` | string |  |
| `account.user_id` | string |  |
| `features` | object |  |
| `meta` | object |  |
| `meta.request_time` | date |  |
| `success` | boolean |  |

## Native endpoint

Through the native Boomlify API, this operation is `GET /api/v1/account/info` (base URL `https://v1.boomlify.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-account-info.md) for the provider-specific parameters and requirements.


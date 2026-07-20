# VoilaNorbert: Get Account

Retrieves current account details from VoilaNorbert.

```
GET https://connect.mindcloud.co/v1/universal/voilaNorbert/latest/actions/get-account
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a VoilaNorbert `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/voilaNorbert/latest/actions/get-account?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/voilaNorbert/latest/actions/get-account?${params}`, {
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
      "admin": true,
      "api_token": "string",
      "avatar_url": "https://example.com",
      "created": "2026-05-07T12:00:00.000Z",
      "credits": {
        "charge_failed": 1,
        "refill_credits": 1,
        "refill_limit": 1,
        "refill_price": 1,
        "remains": 1,
        "total": 1
      },
      "email": "ava@example.com",
      "firstname": "Ava",
      "has_cc": true,
      "is_account_verified": true,
      "language": "string",
      "name": "Ava Chen",
      "optin": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `admin` | boolean |  |
| `api_token` | string |  |
| `avatar_url` | string |  |
| `created` | date |  |
| `credits.charge_failed` | number |  |
| `credits.refill_credits` | number |  |
| `credits.refill_limit` | number |  |
| `credits.refill_price` | number |  |
| `credits.remains` | number |  |
| `credits.total` | number |  |
| `email` | string |  |
| `firstname` | string |  |
| `has_cc` | boolean |  |
| `is_account_verified` | boolean |  |
| `language` | string |  |
| `name` | string |  |
| `optin` | boolean |  |

## Native endpoint

Through the native VoilaNorbert API, this operation is `GET /account/` (base URL `https://api.voilanorbert.com/2018-01-08`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-account.md) for the provider-specific parameters and requirements.


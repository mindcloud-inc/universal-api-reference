# Postalytics: Get My Account

Retrieves your authenticated Postalytics account details.

```
GET https://connect.mindcloud.co/v1/universal/postalytics/latest/actions/get-my-account
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Postalytics `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/postalytics/latest/actions/get-my-account?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/postalytics/latest/actions/get-my-account?${params}`, {
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
      "account_id": 1,
      "address_city": "string",
      "address_state": "string",
      "address_street": "string",
      "address_zip": "string",
      "company": "string",
      "created_date": "string",
      "email_address": "ava@example.com",
      "first_name": "Ava",
      "last_name": "Chen",
      "phone": "string",
      "username": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `account_id` | number | The Postalytics account identifier. |
| `address_city` | string | The city on the account. |
| `address_state` | string | The state on the account. |
| `address_street` | string | The street address on the account. |
| `address_zip` | string | The ZIP or postal code on the account. |
| `company` | string | The company name on the account. |
| `created_date` | string | The account creation date returned by Postalytics. |
| `email_address` | string | The email address on the account. |
| `first_name` | string | The first name on the account. |
| `last_name` | string | The last name on the account. |
| `phone` | string | The phone number on the account. |
| `username` | string | The Postalytics username for the authenticated account. |

## Native endpoint

Through the native Postalytics API, this operation is `GET /api/v1/account/me` (base URL `https://api.postalytics.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-my-account.md) for the provider-specific parameters and requirements.


# SendBox: Get Payment Profile



```
GET https://connect.mindcloud.co/v1/universal/sendBox/latest/actions/get-payment-profile
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SendBox `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sendBox/latest/actions/get-payment-profile?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sendBox/latest/actions/get-payment-profile?${params}`, {
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
      "_id": "string",
      "accounts": [
        {}
      ],
      "bvn": "string",
      "credits": 1,
      "credits_account": {},
      "date_created": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "escrow": 1,
      "escrow_account": {},
      "funds": 1,
      "funds_account": {},
      "last_updated": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "phone": "string",
      "user_id": "string",
      "username": "Ava Chen",
      "virtual_bank_accounts": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_id` | string |  |
| `accounts` | array<object> |  |
| `bvn` | string |  |
| `credits` | number |  |
| `credits_account` | object |  |
| `date_created` | date |  |
| `email` | string |  |
| `escrow` | number |  |
| `escrow_account` | object |  |
| `funds` | number |  |
| `funds_account` | object |  |
| `last_updated` | date |  |
| `name` | string |  |
| `phone` | string |  |
| `user_id` | string |  |
| `username` | string |  |
| `virtual_bank_accounts` | array<object> |  |

## Native endpoint

Through the native SendBox API, this operation is `GET /payments/profile` (base URL `https://live.sendbox.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-payment-profile.md) for the provider-specific parameters and requirements.


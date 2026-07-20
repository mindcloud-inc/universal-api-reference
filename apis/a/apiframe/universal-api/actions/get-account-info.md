# Apiframe: Get Account Info

Retrieves your Apiframe account details and credits.

```
GET https://connect.mindcloud.co/v1/universal/apiframe/latest/actions/get-account-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Apiframe `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/apiframe/latest/actions/get-account-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/apiframe/latest/actions/get-account-info?${params}`, {
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
      "credits": 1,
      "email": "ava@example.com",
      "next_billing_date": "string",
      "plan": "string",
      "subscription_credits": 1,
      "topup_credits": 1,
      "total_images": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `credits` | number |  |
| `email` | string |  |
| `next_billing_date` | string |  |
| `plan` | string |  |
| `subscription_credits` | number |  |
| `topup_credits` | number |  |
| `total_images` | number |  |

## Native endpoint

Through the native Apiframe API, this operation is `GET /account` (base URL `https://api.apiframe.pro`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-account-info.md) for the provider-specific parameters and requirements.


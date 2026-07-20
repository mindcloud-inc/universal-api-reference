# Coast: Get My Account



```
GET https://connect.mindcloud.co/v1/universal/coast/latest/actions/getmyaccount
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Coast `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/coast/latest/actions/getmyaccount?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/coast/latest/actions/getmyaccount?${params}`, {
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
      "address": {},
      "companyEmail": "ava@example.com",
      "id": "string",
      "legalName": "Ava Chen",
      "name": "Ava Chen",
      "settings": {},
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address` | object | Account address |
| `companyEmail` | string | Account email |
| `id` | string | Account identifier |
| `legalName` | string | Legal account name |
| `name` | string | Account name |
| `settings` | object | Account settings |
| `status` | string | Account status |

## Native endpoint

Through the native Coast API, this operation is `GET /v2/account` (base URL `https://public.coastpay.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/getmyaccount.md) for the provider-specific parameters and requirements.


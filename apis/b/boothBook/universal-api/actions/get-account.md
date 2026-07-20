# BoothBook: Get Account

Retrieves account details from BoothBook.

```
GET https://connect.mindcloud.co/v1/universal/boothBook/latest/actions/get-account
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BoothBook `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/boothBook/latest/actions/get-account?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/boothBook/latest/actions/get-account?${params}`, {
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
      "affiliate": "string",
      "business_address": "string",
      "business_admin": "string",
      "business_country": "string",
      "business_name": "Ava Chen",
      "business_postcode": "string",
      "business_timezone": "string",
      "business_website": "string",
      "currency_code": "string",
      "currency_sign": "string",
      "is_paid": 1,
      "plan": "string",
      "result": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `affiliate` | string |  |
| `business_address` | string |  |
| `business_admin` | string |  |
| `business_country` | string |  |
| `business_name` | string |  |
| `business_postcode` | string |  |
| `business_timezone` | string |  |
| `business_website` | string |  |
| `currency_code` | string |  |
| `currency_sign` | string |  |
| `is_paid` | number |  |
| `plan` | string |  |
| `result` | string | BoothBook result status. |

## Native endpoint

Through the native BoothBook API, this operation is `POST /api/v1/get/account` (base URL `https://mindcloud.boothbook.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-account.md) for the provider-specific parameters and requirements.


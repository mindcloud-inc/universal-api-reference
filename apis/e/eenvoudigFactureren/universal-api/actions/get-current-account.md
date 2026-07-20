# EenvoudigFactureren: Get Current Account

Retrieves the current account from EenvoudigFactureren.

```
GET https://connect.mindcloud.co/v1/universal/eenvoudigFactureren/latest/actions/get-current-account
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EenvoudigFactureren `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eenvoudigFactureren/latest/actions/get-current-account?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eenvoudigFactureren/latest/actions/get-current-account?${params}`, {
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
      "account_type": "string",
      "account_type_until": "2026-05-07T12:00:00.000Z",
      "city": "string",
      "company_id": "string",
      "company_name": "Ava Chen",
      "country": "string",
      "created": "2026-05-07T12:00:00.000Z",
      "email_address": "ava@example.com",
      "language": "string",
      "last_login": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "number": "string",
      "postal_code": "string",
      "street": "string",
      "vat_number": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `account_id` | number |  |
| `account_type` | string |  |
| `account_type_until` | date |  |
| `city` | string |  |
| `company_id` | string |  |
| `company_name` | string |  |
| `country` | string |  |
| `created` | date |  |
| `email_address` | string |  |
| `language` | string |  |
| `last_login` | date |  |
| `name` | string |  |
| `number` | string |  |
| `postal_code` | string |  |
| `street` | string |  |
| `vat_number` | string |  |

## Native endpoint

Through the native EenvoudigFactureren API, this operation is `GET /accounts/current` (base URL `https://eenvoudigfactureren.be/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-current-account.md) for the provider-specific parameters and requirements.


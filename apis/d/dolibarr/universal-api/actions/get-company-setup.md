# Dolibarr: Get Company Setup

Retrieves company properties from Dolibarr.

```
GET https://connect.mindcloud.co/v1/universal/dolibarr/latest/actions/get-company-setup
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dolibarr `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dolibarr/latest/actions/get-company-setup?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dolibarr/latest/actions/get-company-setup?${params}`, {
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
      "address": "string",
      "country_code": "string",
      "country_id": 1,
      "currency_code": "string",
      "email": "ava@example.com",
      "entity": 1,
      "id": 1,
      "module": "string",
      "name": "Ava Chen",
      "phone": "string",
      "status": 1,
      "town": "string",
      "url": "https://example.com",
      "zip": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address` | string | Company address. |
| `country_code` | string | Country code. |
| `country_id` | number | Country id. |
| `currency_code` | string | Company currency code. |
| `email` | string | Company email. |
| `entity` | number | Dolibarr entity id. |
| `id` | number | Company setup id. |
| `module` | string | Dolibarr module owning this object. |
| `name` | string | Company name. |
| `phone` | string | Company phone. |
| `status` | number | Company status. |
| `town` | string | Town/city. |
| `url` | string | Company website URL. |
| `zip` | string | Postal code. |

## Native endpoint

Through the native Dolibarr API, this operation is `GET /setup/company` (base URL `https://mindcloud-dolibarr-0421.with7.dolicloud.com/api/index.php`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-company-setup.md) for the provider-specific parameters and requirements.


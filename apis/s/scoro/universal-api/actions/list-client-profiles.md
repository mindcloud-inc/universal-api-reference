# Scoro: List Client Profiles

Retrieves client profiles from Scoro.

```
GET https://connect.mindcloud.co/v1/universal/scoro/latest/actions/list-client-profiles
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Scoro `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scoro/latest/actions/list-client-profiles?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scoro/latest/actions/list-client-profiles?${params}`, {
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
      "created_date": {},
      "currency": "string",
      "deadline_days": 1,
      "discount": "string",
      "fine": "string",
      "id": 1,
      "modified_date": {},
      "name": "Ava Chen",
      "payment_type": "string",
      "price_list_id": 1,
      "vat_code_id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_date` | object | Created timestamp. |
| `currency` | string | Currency. |
| `deadline_days` | number | Default deadline in days. |
| `discount` | string | Default discount. |
| `fine` | string | Late fine settings. |
| `id` | number | Client profile ID. |
| `modified_date` | object | Modified timestamp. |
| `name` | string | Client profile name. |
| `payment_type` | string | Payment type. |
| `price_list_id` | number | Price list ID. |
| `vat_code_id` | number | VAT code ID. |

## Native endpoint

Through the native Scoro API, this operation is `POST clientProfiles/list` (base URL `{{credentials.subdomain}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-client-profiles.md) for the provider-specific parameters and requirements.


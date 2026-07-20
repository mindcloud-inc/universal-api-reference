# Paystack: List Countries



```
GET https://connect.mindcloud.co/v1/universal/paystack/latest/actions/list-countries
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Paystack `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/paystack/latest/actions/list-countries?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/paystack/latest/actions/list-countries?${params}`, {
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
      "active_for_dashboard_onboarding": true,
      "calling_code": "string",
      "default_currency_code": "string",
      "id": 1,
      "iso_code": "string",
      "name": "Ava Chen",
      "pilot_mode": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active_for_dashboard_onboarding` | boolean |  |
| `calling_code` | string |  |
| `default_currency_code` | string |  |
| `id` | number |  |
| `iso_code` | string |  |
| `name` | string |  |
| `pilot_mode` | boolean |  |

## Native endpoint

Through the native Paystack API, this operation is `GET /country` (base URL `https://api.paystack.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-countries.md) for the provider-specific parameters and requirements.


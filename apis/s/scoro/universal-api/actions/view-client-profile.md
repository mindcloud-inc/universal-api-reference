# Scoro: View Client Profile

Retrieves client profile details from Scoro.

```
GET https://connect.mindcloud.co/v1/universal/scoro/latest/actions/view-client-profile
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Scoro `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scoro/latest/actions/view-client-profile?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scoro/latest/actions/view-client-profile?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | no | Scoro client profile ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_date": "string",
      "currency": "string",
      "deadline_days": 1,
      "discount": "string",
      "fine": "string",
      "id": 1,
      "modified_date": "string",
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
| `created_date` | string |  |
| `currency` | string |  |
| `deadline_days` | number |  |
| `discount` | string |  |
| `fine` | string |  |
| `id` | number |  |
| `modified_date` | string |  |
| `name` | string |  |
| `payment_type` | string |  |
| `price_list_id` | number |  |
| `vat_code_id` | number |  |

## Native endpoint

Through the native Scoro API, this operation is `POST clientProfiles/view/:id` (base URL `{{credentials.subdomain}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/view-client-profile.md) for the provider-specific parameters and requirements.


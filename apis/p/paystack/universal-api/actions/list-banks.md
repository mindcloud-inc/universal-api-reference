# Paystack: List Banks



```
GET https://connect.mindcloud.co/v1/universal/paystack/latest/actions/list-banks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Paystack `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/paystack/latest/actions/list-banks?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/paystack/latest/actions/list-banks?${params}`, {
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
| `country` | string | no |  |
| `currency` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "code": "string",
      "country": "string",
      "currency": "string",
      "id": 1,
      "longcode": "string",
      "name": "Ava Chen",
      "slug": "string",
      "supports_transfer": true,
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `code` | string |  |
| `country` | string |  |
| `currency` | string |  |
| `id` | number |  |
| `longcode` | string |  |
| `name` | string |  |
| `slug` | string |  |
| `supports_transfer` | boolean |  |
| `type` | string |  |

## Native endpoint

Through the native Paystack API, this operation is `GET /bank` (base URL `https://api.paystack.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-banks.md) for the provider-specific parameters and requirements.


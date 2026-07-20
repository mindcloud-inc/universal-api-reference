# Chargback: Get Business Account



```
GET https://connect.mindcloud.co/v1/universal/chargback/latest/actions/get-business-account
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chargback `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chargback/latest/actions/get-business-account?connectionId=$CONNECTION_ID&external_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "external_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chargback/latest/actions/get-business-account?${params}`, {
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
| `external_id` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "base_currency": "string",
      "created": "string",
      "external_id": "string",
      "is_active": true,
      "is_demo": true,
      "name": "Ava Chen",
      "updated": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `base_currency` | string | Base currency for the business account. |
| `created` | string | Business account creation timestamp. |
| `external_id` | string | Chargeback business-account external identifier. |
| `is_active` | boolean | Whether the business account is active. |
| `is_demo` | boolean | Whether the business account is demo data. |
| `name` | string | Business account name. |
| `updated` | string | Business account last update timestamp. |
| `url` | string | Business account website URL. |

## Native endpoint

Through the native Chargback API, this operation is `GET /api/public/v1/business_accounts/:external_id/` (base URL `https://api.chargeback.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-business-account.md) for the provider-specific parameters and requirements.


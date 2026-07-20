# Voucherify: Get Validation Rule

Retrieves a validation rule from Voucherify.

```
GET https://connect.mindcloud.co/v1/universal/voucherify/latest/actions/get-validation-rule
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Voucherify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/voucherify/latest/actions/get-validation-rule?connectionId=$CONNECTION_ID&validationRuleId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "validationRuleId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/voucherify/latest/actions/get-validation-rule?${params}`, {
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
| `validationRuleId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "applicableTo": {},
      "bundleRules": {},
      "createdAt": "string",
      "id": "string",
      "name": "Ava Chen",
      "object": "string",
      "rules": {},
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `applicableTo` | object |  |
| `bundleRules` | object |  |
| `createdAt` | string |  |
| `id` | string |  |
| `name` | string |  |
| `object` | string |  |
| `rules` | object |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native Voucherify API, this operation is `GET /validation-rules/:validationRuleId` (base URL `https://us1.api.voucherify.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-validation-rule.md) for the provider-specific parameters and requirements.


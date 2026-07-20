# Tax ID Pro: Batch Validate Tax IDs

Creates batch tax ID validations in Tax ID Pro.

```
POST https://connect.mindcloud.co/v1/universal/taxIDPro/latest/actions/batch-validate-tax-ids
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tax ID Pro `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/taxIDPro/latest/actions/batch-validate-tax-ids" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "validations[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/taxIDPro/latest/actions/batch-validate-tax-ids', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "validations[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `validations[]` | array<object> | yes | Array of tax ID validation objects. Each item must include reference_id, country, and tin; type is optional and may be individual, entity, or vat. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `isIrs` | boolean | no | Set true when country values use IRS country codes instead of ISO country codes. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "country_name": "Ava Chen",
      "error_code": "string",
      "format_name": "Ava Chen",
      "is_valid": true,
      "message": "string",
      "reference_id": "string",
      "tin_compact": "string",
      "tin_standard": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `country_name` | string | Country name for the tax ID format that was evaluated, when returned. |
| `error_code` | string | Item-level error code for unsupported country/type combinations or other item issues; null when absent. |
| `format_name` | string | Name of the tax ID format that matched or was evaluated. |
| `is_valid` | boolean | Whether the tax ID is valid for the requested country and type. |
| `message` | string | Validation guidance when the tax ID is invalid; null when valid or unsupported. |
| `reference_id` | string | Caller-provided identifier used to match each response row to its request item. |
| `tin_compact` | string | Validated tax ID value in compact form when valid; null when unavailable. |
| `tin_standard` | string | Validated tax ID value in standard display format when valid; null when unavailable. |

## Native endpoint

Through the native Tax ID Pro API, this operation is `POST /validate` (base URL `https://v3.api.taxid.pro`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/batch-validate-tax-ids.md) for the provider-specific parameters and requirements.


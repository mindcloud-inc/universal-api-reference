# Tax ID Pro: Validate Tax ID

Retrieves a tax ID validation from Tax ID Pro.

```
GET https://connect.mindcloud.co/v1/universal/taxIDPro/latest/actions/validate-tax-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tax ID Pro `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/taxIDPro/latest/actions/validate-tax-id?connectionId=$CONNECTION_ID&country=string&tin=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "country": "string",
  "tin": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/taxIDPro/latest/actions/validate-tax-id?${params}`, {
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
| `country` | string | yes | Two-letter country code as defined in the ISO standard. Use IRS country codes only when Is IRS is true. |
| `tin` | string | yes | Tax ID number. It may contain numbers, letters, dots, dashes, or slashes when those separators match the tax ID format being tested. |
| `type` | string | no | Optional tax ID type. Use individual, entity, or vat; omit to test all available types for the country. One of: `0`, `1`, `2`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `locale` | string | no | Optional language tag for the message property. Use auto for the language most appropriate for the country, or one of the documented locales. One of: `0`, `1`, `2`, `3`, `4`, `5`, `6`, `7`, `8`. |
| `isIrs` | boolean | no | Set true when country uses IRS country codes instead of ISO country codes. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "country_name": "Ava Chen",
      "format_name": "Ava Chen",
      "is_valid": true,
      "message": "string",
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
| `country_name` | string | Country name for the tax ID format that was evaluated. |
| `format_name` | string | Name of the tax ID format that matched or was evaluated. |
| `is_valid` | boolean | Whether the provided tax ID is valid for the requested country and type. |
| `message` | string | Validation guidance when the tax ID is invalid; null when valid. |
| `tin_compact` | string | Validated tax ID value in compact form when valid; null when unavailable. |
| `tin_standard` | string | Validated tax ID value in standard display format when valid; null when unavailable. |

## Native endpoint

Through the native Tax ID Pro API, this operation is `GET /validate` (base URL `https://v3.api.taxid.pro`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/validate-tax-id.md) for the provider-specific parameters and requirements.


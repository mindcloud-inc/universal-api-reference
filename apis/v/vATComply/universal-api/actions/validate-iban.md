# VAT Comply: Validate IBAN

Validates an IBAN in VAT Comply.

```
GET https://connect.mindcloud.co/v1/universal/vATComply/latest/actions/validate-iban
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a VAT Comply `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vATComply/latest/actions/validate-iban?connectionId=$CONNECTION_ID&iban=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "iban": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vATComply/latest/actions/validate-iban?${params}`, {
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
| `iban` | string | yes | The IBAN to validate. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "account_number": "string",
      "bank_code": "string",
      "bank_name": "Ava Chen",
      "bban": "string",
      "bic": "string",
      "branch_code": "string",
      "checksum_digits": "string",
      "country_code": "string",
      "country_name": "Ava Chen",
      "iban": "string",
      "in_sepa_zone": true,
      "valid": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `account_number` | string |  |
| `bank_code` | string |  |
| `bank_name` | string |  |
| `bban` | string |  |
| `bic` | string |  |
| `branch_code` | string |  |
| `checksum_digits` | string |  |
| `country_code` | string |  |
| `country_name` | string |  |
| `iban` | string |  |
| `in_sepa_zone` | boolean |  |
| `valid` | boolean |  |

## Native endpoint

Through the native VAT Comply API, this operation is `GET /iban` (base URL `https://api.vatcomply.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/validate-iban.md) for the provider-specific parameters and requirements.


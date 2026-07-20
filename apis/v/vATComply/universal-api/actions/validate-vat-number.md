# VAT Comply: Validate VAT Number

Validates a VAT number in VAT Comply.

```
GET https://connect.mindcloud.co/v1/universal/vATComply/latest/actions/validate-vat-number
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a VAT Comply `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vATComply/latest/actions/validate-vat-number?connectionId=$CONNECTION_ID&vatNumber=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "vatNumber": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vATComply/latest/actions/validate-vat-number?${params}`, {
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
| `vatNumber` | string | yes | The VAT number to validate. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address": "string",
      "country_code": "string",
      "name": "Ava Chen",
      "valid": true,
      "vat_number": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address` | string |  |
| `country_code` | string |  |
| `name` | string |  |
| `valid` | boolean |  |
| `vat_number` | string |  |

## Native endpoint

Through the native VAT Comply API, this operation is `GET /vat` (base URL `https://api.vatcomply.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/validate-vat-number.md) for the provider-specific parameters and requirements.


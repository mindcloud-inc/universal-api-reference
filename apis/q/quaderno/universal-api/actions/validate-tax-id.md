# Quaderno: Validate Tax ID

Validates a tax ID in Quaderno.

```
GET https://connect.mindcloud.co/v1/universal/quaderno/latest/actions/validate-tax-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Quaderno `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/quaderno/latest/actions/validate-tax-id?connectionId=$CONNECTION_ID&country=FR" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "country": "FR"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/quaderno/latest/actions/validate-tax-id?${params}`, {
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
| `country` | string | yes | Two-letter ISO country code for the tax ID. Example: `FR`. |
| `taxId` | string | no | Tax ID value to validate. Example: `FR40303265045`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "valid": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `valid` | boolean |  |

## Native endpoint

Through the native Quaderno API, this operation is `GET /tax_ids/validate` (base URL `https://sandbox-quadernoapp.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/validate-tax-id.md) for the provider-specific parameters and requirements.


# Abstract IBAN Validator: Validate IBAN



```
GET https://connect.mindcloud.co/v1/universal/abstractIBANValidator/latest/actions/validate-iban
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Abstract IBAN Validator `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/abstractIBANValidator/latest/actions/validate-iban?connectionId=$CONNECTION_ID&iban=BE71096123456769" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "iban": "BE71096123456769"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/abstractIBANValidator/latest/actions/validate-iban?${params}`, {
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
| `iban` | string | yes | International Bank Account Number to validate. Abstract accepts whitespace in the IBAN value. Default: `BE71096123456769`. Example: `BE71096123456769`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "iban": "string",
      "isValid": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `iban` | string | The IBAN submitted for validation. |
| `isValid` | boolean | Whether Abstract determined the submitted IBAN is valid. |

## Native endpoint

Through the native Abstract IBAN Validator API, this operation is `GET /v1/` (base URL `https://ibanvalidation.abstractapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/validate-iban.md) for the provider-specific parameters and requirements.


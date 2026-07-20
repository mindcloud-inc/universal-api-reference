# Cloudmersive Data Validation: Validate Email Address Syntax Only

Validates email address syntax with Cloudmersive Data Validation.

```
GET https://connect.mindcloud.co/v1/universal/cloudmersiveDataValidation/latest/actions/validate-email-address-syntax-only
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cloudmersive Data Validation `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cloudmersiveDataValidation/latest/actions/validate-email-address-syntax-only?connectionId=$CONNECTION_ID&value=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "value": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cloudmersiveDataValidation/latest/actions/validate-email-address-syntax-only?${params}`, {
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
| `value` | string | yes | Email address to validate syntactically. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Domain": "string",
      "IsDisposable": true,
      "IsFreeEmailProvider": true,
      "ValidAddress": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Domain` | string |  |
| `IsDisposable` | boolean |  |
| `IsFreeEmailProvider` | boolean |  |
| `ValidAddress` | boolean |  |

## Native endpoint

Through the native Cloudmersive Data Validation API, this operation is `POST /validate/email/address/syntaxOnly` (base URL `https://api.cloudmersive.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/validate-email-address-syntax-only.md) for the provider-specific parameters and requirements.


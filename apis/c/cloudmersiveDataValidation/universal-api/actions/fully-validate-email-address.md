# Cloudmersive Data Validation: Fully Validate Email Address

Fully validates an email address with Cloudmersive Data Validation.

```
GET https://connect.mindcloud.co/v1/universal/cloudmersiveDataValidation/latest/actions/fully-validate-email-address
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cloudmersive Data Validation `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cloudmersiveDataValidation/latest/actions/fully-validate-email-address?connectionId=$CONNECTION_ID&email=ava%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "email": "ava@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cloudmersiveDataValidation/latest/actions/fully-validate-email-address?${params}`, {
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
| `email` | string | yes | Email address to fully validate. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Domain": "string",
      "IsCatchallDomain": true,
      "IsDisposable": true,
      "IsFreeEmailProvider": true,
      "MailServerUsedForValidation": "string",
      "Valid_Domain": true,
      "Valid_SMTP": true,
      "Valid_Syntax": true,
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
| `IsCatchallDomain` | boolean |  |
| `IsDisposable` | boolean |  |
| `IsFreeEmailProvider` | boolean |  |
| `MailServerUsedForValidation` | string |  |
| `Valid_Domain` | boolean |  |
| `Valid_SMTP` | boolean |  |
| `Valid_Syntax` | boolean |  |
| `ValidAddress` | boolean |  |

## Native endpoint

Through the native Cloudmersive Data Validation API, this operation is `POST /validate/email/address/full` (base URL `https://api.cloudmersive.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/fully-validate-email-address.md) for the provider-specific parameters and requirements.


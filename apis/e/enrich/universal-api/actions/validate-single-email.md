# Enrich.so: Validate a Single Email

Validates an email address in Enrich.so.

```
GET https://connect.mindcloud.co/v1/universal/enrich/latest/actions/validate-single-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Enrich.so `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/enrich/latest/actions/validate-single-email?connectionId=$CONNECTION_ID&email=sarah.chen%40stripe.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "email": "sarah.chen@stripe.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/enrich/latest/actions/validate-single-email?${params}`, {
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
| `email` | string | yes | Email address to validate. Default: `sarah.chen@stripe.com`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "confidence": "string",
      "email": "ava@example.com",
      "hasSEG": true,
      "isCatchAll": true,
      "isFederated": true,
      "message": "string",
      "provider": "string",
      "result": "string",
      "segProvider": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `confidence` | string | Confidence level for the validation result. |
| `email` | string | Email address that was validated. |
| `hasSEG` | boolean | Whether a secure email gateway was detected. |
| `isCatchAll` | boolean | Whether the domain is catch-all. |
| `isFederated` | boolean | Whether the mailbox uses federated identity. |
| `message` | string | Provider explanation for the validation result. |
| `provider` | string | Detected mail provider. |
| `result` | string | Validation result such as valid, invalid, or risky. |
| `segProvider` | string | Detected secure email gateway provider. |

## Native endpoint

Through the native Enrich.so API, this operation is `POST /email-validation` (base URL `https://dev.enrich.so/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/validate-single-email.md) for the provider-specific parameters and requirements.


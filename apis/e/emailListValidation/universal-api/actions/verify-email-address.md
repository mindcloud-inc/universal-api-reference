# Email List Validation: Verify Email Address



```
GET https://connect.mindcloud.co/v1/universal/emailListValidation/latest/actions/verify-email-address
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Email List Validation `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/emailListValidation/latest/actions/verify-email-address?connectionId=$CONNECTION_ID&email=test%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "email": "test@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/emailListValidation/latest/actions/verify-email-address?${params}`, {
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
| `email` | string | yes | Email address to verify. Example: `test@example.com`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "result": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `result` | string | Plain-text verification result returned by Email List Validation, such as valid, invalid, unknown, disposable, role, free, accept all, timeout, or error. |

## Native endpoint

Through the native Email List Validation API, this operation is `GET /api/verifEmail` (base URL `https://app.emaillistvalidation.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/verify-email-address.md) for the provider-specific parameters and requirements.


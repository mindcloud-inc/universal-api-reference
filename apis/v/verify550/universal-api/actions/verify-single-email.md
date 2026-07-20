# Verify550: Verify Single Email

Verifies a single email address with Verify550.

```
GET https://connect.mindcloud.co/v1/universal/verify550/latest/actions/verify-single-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Verify550 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/verify550/latest/actions/verify-single-email?connectionId=$CONNECTION_ID&email=ava%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "email": "ava@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/verify550/latest/actions/verify-single-email?${params}`, {
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
| `email` | string | yes | Email address to verify. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "result": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string | Optional provider message returned with the verification result. |
| `result` | string | Verify550 verification result code for the email address. |
| `success` | boolean | Whether Verify550 handled the email verification request successfully. |

## Native endpoint

Through the native Verify550 API, this operation is `GET /singlemail` (base URL `https://app.verify550.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/verify-single-email.md) for the provider-specific parameters and requirements.


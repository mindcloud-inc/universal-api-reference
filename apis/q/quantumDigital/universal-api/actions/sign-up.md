# Quantum Digital: Sign Up



```
POST https://connect.mindcloud.co/v1/universal/quantumDigital/latest/actions/sign-up
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Quantum Digital `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/quantumDigital/latest/actions/sign-up" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "accountName": "Ava Chen",
  "email": "ava@example.com",
  "recaptchaToken": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/quantumDigital/latest/actions/sign-up', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "accountName": "Ava Chen",
    "email": "ava@example.com",
    "recaptchaToken": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `accountName` | string | yes |  |
| `email` | string | yes |  |
| `recaptchaToken` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cc_form_link": "https://example.com",
      "errorMsg": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cc_form_link` | string | Link to the credit-card form used by the provider. |
| `errorMsg` | string | Error message returned by the provider. |
| `success` | boolean | Whether the sign-up request succeeded. |

## Native endpoint

Through the native Quantum Digital API, this operation is `POST /devplatform/signup` (base URL `https://api.quantumdigital.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/sign-up.md) for the provider-specific parameters and requirements.


# Formspark: Submit Form With Redirect

Creates a Formspark form submission with redirect settings.

```
POST https://connect.mindcloud.co/v1/universal/formspark/latest/actions/submit-form-with-redirect
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Formspark `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/formspark/latest/actions/submit-form-with-redirect" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "formId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/formspark/latest/actions/submit-form-with-redirect', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "formId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `formId` | string | yes | The Formspark form ID or the special `echo` endpoint for validation. |
| `email` | string | no | Optional email field to include in the submission body. |
| `message` | string | no | Optional message field to include in the submission body. |
| `_redirect` | string | no | Custom URL to redirect the browser to after a successful submission. |
| `_append` | string | no | Whether Formspark should append submitted values to the redirect URL. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_append": "string",
      "_redirect": "https://example.com",
      "email": "ava@example.com",
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_append` | string | Whether redirect query appending is enabled. |
| `_redirect` | string | Configured success redirect URL. |
| `email` | string | Echoed email field. |
| `message` | string | Echoed message field. |

## Native endpoint

Through the native Formspark API, this operation is `POST :formId` (base URL `https://submit-form.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/submit-form-with-redirect.md) for the provider-specific parameters and requirements.


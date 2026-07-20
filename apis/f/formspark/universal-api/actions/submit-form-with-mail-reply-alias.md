# Formspark: Submit Form With Mail Reply Alias

Creates a Formspark form submission using the mail reply alias.

```
POST https://connect.mindcloud.co/v1/universal/formspark/latest/actions/submit-form-with-mail-reply-alias
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Formspark `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/formspark/latest/actions/submit-form-with-mail-reply-alias" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "formId": "string",
  "mail": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/formspark/latest/actions/submit-form-with-mail-reply-alias', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "formId": "string",
    "mail": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `formId` | string | yes | Formspark form ID or the special `echo` endpoint for validation. |
| `mail` | string | yes | Email address used as the direct-reply target. |
| `message` | string | no | Submitted message body. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "mail": "ava@example.com",
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `mail` | string | Echoed mail alias value. |
| `message` | string | Echoed message field. |

## Native endpoint

Through the native Formspark API, this operation is `POST :formId` (base URL `https://submit-form.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/submit-form-with-mail-reply-alias.md) for the provider-specific parameters and requirements.


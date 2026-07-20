# Formspark: Submit Form With Feedback Messages

Creates a Formspark form submission with custom feedback messages.

```
POST https://connect.mindcloud.co/v1/universal/formspark/latest/actions/submit-form-with-feedback-messages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Formspark `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/formspark/latest/actions/submit-form-with-feedback-messages" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "formId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/formspark/latest/actions/submit-form-with-feedback-messages', {
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
| `message` | string | no | Optional message field to include in the submission body. |
| `_feedback.success.title` | string | no | Custom success title for the hosted Formspark feedback page. |
| `_feedback.success.message` | string | no | Custom success message for the hosted Formspark feedback page. |
| `_feedback.error.title` | string | no | Custom error title for the hosted Formspark feedback page. |
| `_feedback.error.message` | string | no | Custom error message for the hosted Formspark feedback page. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_feedback": {
        "error": {
          "message": "string",
          "title": "string"
        },
        "success": {
          "message": "string",
          "title": "string"
        }
      },
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_feedback.error.message` | string | Custom error-page message. |
| `_feedback.error.title` | string | Custom error-page title. |
| `_feedback.success.message` | string | Custom success-page message. |
| `_feedback.success.title` | string | Custom success-page title. |
| `message` | string | Echoed message field. |

## Native endpoint

Through the native Formspark API, this operation is `POST :formId` (base URL `https://submit-form.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/submit-form-with-feedback-messages.md) for the provider-specific parameters and requirements.


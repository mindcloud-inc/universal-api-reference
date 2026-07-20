# Formspark: Submit Form With Feedback Page

Creates a Formspark form submission with feedback page settings.

```
POST https://connect.mindcloud.co/v1/universal/formspark/latest/actions/submit-form-with-feedback-page
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Formspark `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/formspark/latest/actions/submit-form-with-feedback-page" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "formId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/formspark/latest/actions/submit-form-with-feedback-page', {
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
| `_feedback.whitelabel` | string | no | Remove Formspark branding from the feedback page when the workspace plan supports it. |
| `_feedback.dark` | string | no | Toggle dark mode on the hosted Formspark feedback page. |
| `_feedback.language` | string | no | Language code for the hosted Formspark feedback page. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_feedback": {
        "dark": "string",
        "language": "string",
        "whitelabel": "string"
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
| `_feedback.dark` | string | Dark-mode toggle for the feedback page. |
| `_feedback.language` | string | Feedback page language code. |
| `_feedback.whitelabel` | string | Whitelabel toggle for the feedback page. |
| `message` | string | Echoed message field. |

## Native endpoint

Through the native Formspark API, this operation is `POST :formId` (base URL `https://submit-form.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/submit-form-with-feedback-page.md) for the provider-specific parameters and requirements.


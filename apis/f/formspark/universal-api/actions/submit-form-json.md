# Formspark: Submit Form JSON

Creates a Formspark form submission from a JSON payload.

```
POST https://connect.mindcloud.co/v1/universal/formspark/latest/actions/submit-form-json
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Formspark `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/formspark/latest/actions/submit-form-json" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "formId": "your-form-id"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/formspark/latest/actions/submit-form-json', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "formId": "your-form-id"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `formId` | string | yes | The Formspark form ID from the hosted endpoint URL, for example `your-form-id` in `https://submit-form.com/your-form-id`. Example: `your-form-id`. |
| `email` | string | no | Optional email field to include in the submission body. |
| `message` | string | no | Optional message field to include in the submission body. |
| `name` | string | no | Optional display name field to include in the submission body. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "email": "ava@example.com",
      "message": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `email` | string | Echoed email value when an email field is submitted. |
| `message` | string | Echoed message value from the submitted payload. |
| `name` | string | Echoed display name value when present. |

## Native endpoint

Through the native Formspark API, this operation is `POST :formId` (base URL `https://submit-form.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/submit-form-json.md) for the provider-specific parameters and requirements.


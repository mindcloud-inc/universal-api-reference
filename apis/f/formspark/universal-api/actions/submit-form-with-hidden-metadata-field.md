# Formspark: Submit Form With Hidden Metadata Field

Creates a Formspark form submission with a hidden metadata field.

```
POST https://connect.mindcloud.co/v1/universal/formspark/latest/actions/submit-form-with-hidden-metadata-field
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Formspark `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/formspark/latest/actions/submit-form-with-hidden-metadata-field" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "formId": "string",
  "website-version": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/formspark/latest/actions/submit-form-with-hidden-metadata-field', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "formId": "string",
    "website-version": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `formId` | string | yes | Formspark form ID or the special `echo` endpoint for validation. |
| `website-version` | string | yes | Example hidden metadata field value. |
| `name` | string | no | Visible user-entered field submitted alongside metadata. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "name": "Ava Chen",
      "website-version": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `name` | string | Echoed visible user-entered field. |
| `website-version` | string | Echoed hidden metadata field. |

## Native endpoint

Through the native Formspark API, this operation is `POST :formId` (base URL `https://submit-form.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/submit-form-with-hidden-metadata-field.md) for the provider-specific parameters and requirements.


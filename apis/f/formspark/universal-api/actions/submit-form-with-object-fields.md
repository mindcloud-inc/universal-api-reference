# Formspark: Submit Form With Object Fields

Creates a Formspark form submission with object fields.

```
POST https://connect.mindcloud.co/v1/universal/formspark/latest/actions/submit-form-with-object-fields
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Formspark `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/formspark/latest/actions/submit-form-with-object-fields" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "formId": "string",
  "contact.name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/formspark/latest/actions/submit-form-with-object-fields', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "formId": "string",
    "contact.name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `formId` | string | yes | Formspark form ID or the special `echo` endpoint for validation. |
| `contact.name` | string | yes | Dotted object field for a nested contact name. |
| `contact.email` | string | no | Dotted object field for a nested contact email. |
| `company.name` | string | no | Dotted object field for a nested company name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "company": {
        "name": "Ava Chen"
      },
      "contact": {
        "email": "ava@example.com",
        "name": "Ava Chen"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `company.name` | string | Echoed nested company name. |
| `contact.email` | string | Echoed nested contact email. |
| `contact.name` | string | Echoed nested contact name. |

## Native endpoint

Through the native Formspark API, this operation is `POST :formId` (base URL `https://submit-form.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/submit-form-with-object-fields.md) for the provider-specific parameters and requirements.


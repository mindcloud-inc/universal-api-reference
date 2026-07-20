# Formspark: Submit Form With Multi Select

Creates a Formspark form submission with multiple selected values.

```
POST https://connect.mindcloud.co/v1/universal/formspark/latest/actions/submit-form-with-multi-select
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Formspark `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/formspark/latest/actions/submit-form-with-multi-select" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "formId": "string",
  "cars[0]": "string",
  "cars[1]": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/formspark/latest/actions/submit-form-with-multi-select', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "formId": "string",
    "cars[0]": "string",
    "cars[1]": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `formId` | string | yes | Formspark form ID or the special `echo` endpoint for validation. |
| `message` | string | no | Submitted message body. |
| `cars[0]` | string | yes | First selected option. |
| `cars[1]` | string | yes | Second selected option. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cars[0]": "string",
      "cars[1]": "string",
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cars[0]` | string | Echoed first selected option. |
| `cars[1]` | string | Echoed second selected option. |
| `message` | string | Echoed message field. |

## Native endpoint

Through the native Formspark API, this operation is `POST :formId` (base URL `https://submit-form.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/submit-form-with-multi-select.md) for the provider-specific parameters and requirements.


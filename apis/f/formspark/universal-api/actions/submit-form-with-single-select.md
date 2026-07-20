# Formspark: Submit Form With Single Select

Creates a Formspark form submission with a single select value.

```
POST https://connect.mindcloud.co/v1/universal/formspark/latest/actions/submit-form-with-single-select
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Formspark `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/formspark/latest/actions/submit-form-with-single-select" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "formId": "string",
  "car": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/formspark/latest/actions/submit-form-with-single-select', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "formId": "string",
    "car": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `formId` | string | yes | Formspark form ID or the special `echo` endpoint for validation. |
| `car` | string | yes | Single selected drop-down value. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "car": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `car` | string | Echoed selected drop-down value. |

## Native endpoint

Through the native Formspark API, this operation is `POST :formId` (base URL `https://submit-form.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/submit-form-with-single-select.md) for the provider-specific parameters and requirements.


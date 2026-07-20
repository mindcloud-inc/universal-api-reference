# Formspark: Submit Form With Extended UTM Parameters

Creates a Formspark form submission with extended UTM parameters.

```
POST https://connect.mindcloud.co/v1/universal/formspark/latest/actions/submit-form-with-extended-utm-parameters
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Formspark `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/formspark/latest/actions/submit-form-with-extended-utm-parameters" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "formId": "string",
  "utm_source": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/formspark/latest/actions/submit-form-with-extended-utm-parameters', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "formId": "string",
    "utm_source": "string"
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
| `utm_source` | string | yes | Traffic source. |
| `utm_medium` | string | no | Traffic medium. |
| `utm_campaign` | string | no | Campaign name. |
| `utm_term` | string | no | Paid-search keyword term. |
| `utm_content` | string | no | Ad or content variant identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "utm_campaign": "string",
      "utm_content": "string",
      "utm_medium": "string",
      "utm_source": "string",
      "utm_term": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string | Echoed message field. |
| `utm_campaign` | string | Echoed campaign name. |
| `utm_content` | string | Echoed content variant. |
| `utm_medium` | string | Echoed traffic medium. |
| `utm_source` | string | Echoed traffic source. |
| `utm_term` | string | Echoed keyword term. |

## Native endpoint

Through the native Formspark API, this operation is `POST :formId` (base URL `https://submit-form.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/submit-form-with-extended-utm-parameters.md) for the provider-specific parameters and requirements.


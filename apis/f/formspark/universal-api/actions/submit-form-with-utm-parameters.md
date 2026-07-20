# Formspark: Submit Form With UTM Parameters

Creates a Formspark form submission with UTM tracking parameters.

```
POST https://connect.mindcloud.co/v1/universal/formspark/latest/actions/submit-form-with-utm-parameters
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Formspark `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/formspark/latest/actions/submit-form-with-utm-parameters" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "formId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/formspark/latest/actions/submit-form-with-utm-parameters', {
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
| `utm_source` | string | no | UTM source attribution value. |
| `utm_medium` | string | no | UTM medium attribution value. |
| `utm_campaign` | string | no | UTM campaign attribution value. |
| `ref` | string | no | Custom referral source field supported by Formtrack. |
| `referrer` | string | no | Custom referrer field supported by Formtrack. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "ref": "string",
      "referrer": "string",
      "utm_campaign": "string",
      "utm_medium": "string",
      "utm_source": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string | Echoed message field. |
| `ref` | string | Custom ref field. |
| `referrer` | string | Custom referrer field. |
| `utm_campaign` | string | UTM campaign value. |
| `utm_medium` | string | UTM medium value. |
| `utm_source` | string | UTM source value. |

## Native endpoint

Through the native Formspark API, this operation is `POST :formId` (base URL `https://submit-form.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/submit-form-with-utm-parameters.md) for the provider-specific parameters and requirements.


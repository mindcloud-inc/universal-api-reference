# Typeform: Update Form Translation



```
PUT https://connect.mindcloud.co/v1/universal/typeform/latest/actions/update-form-translation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Typeform `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/typeform/latest/actions/update-form-translation" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "formId": "string",
  "language": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/typeform/latest/actions/update-form-translation', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "formId": "string",
    "language": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fields` | string | no | Translated fields payload. |
| `formId` | string | yes | Typeform form identifier. |
| `language` | string | yes | Language code. |
| `messages` | string | no | Translated messages payload. |
| `thankyouScreens` | string | no | Translated thank-you screens payload. |
| `welcomeScreens` | string | no | Translated welcome screens payload. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "value": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `value` | string | Empty response body returned when the form translation is updated successfully. |

## Native endpoint

Through the native Typeform API, this operation is `PUT /forms/:formId/translations/:language` (base URL `https://api.typeform.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-form-translation.md) for the provider-specific parameters and requirements.


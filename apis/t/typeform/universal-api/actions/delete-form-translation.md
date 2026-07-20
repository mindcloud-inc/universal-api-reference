# Typeform: Delete Form Translation



```
DELETE https://connect.mindcloud.co/v1/universal/typeform/latest/actions/delete-form-translation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Typeform `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/typeform/latest/actions/delete-form-translation?connectionId=$CONNECTION_ID&formId=string&language=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "formId": "string",
  "language": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/typeform/latest/actions/delete-form-translation?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `formId` | string | yes | Typeform form identifier. |
| `language` | string | yes | Language code. |

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
| `value` | string | Empty response body returned when the form translation is deleted successfully. |

## Native endpoint

Through the native Typeform API, this operation is `DELETE /forms/:formId/translations/:language` (base URL `https://api.typeform.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-form-translation.md) for the provider-specific parameters and requirements.


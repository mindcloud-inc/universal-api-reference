# Jotform: Get Form Properties

Retrieves properties for a Jotform form.

```
GET https://connect.mindcloud.co/v1/universal/jotform/latest/actions/get-form-properties
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Jotform `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/jotform/latest/actions/get-form-properties?connectionId=$CONNECTION_ID&formId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "formId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/jotform/latest/actions/get-form-properties?${params}`, {
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
| `formId` | string | yes | Form ID |

## Response

```json
{
  "success": true,
  "data": [
    {
      "formType": "string",
      "id": "string",
      "status": "string",
      "thanktext": "string",
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `formType` | string |  |
| `id` | string |  |
| `status` | string |  |
| `thanktext` | string |  |
| `title` | string |  |

## Native endpoint

Through the native Jotform API, this operation is `GET /form/:formId/properties` (base URL `https://api.jotform.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-form-properties.md) for the provider-specific parameters and requirements.


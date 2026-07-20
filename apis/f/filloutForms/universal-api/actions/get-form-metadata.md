# Fillout Forms: Get Form Metadata

Retrieves metadata for a Fillout form.

```
GET https://connect.mindcloud.co/v1/universal/filloutForms/latest/actions/get-form-metadata
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fillout Forms `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/filloutForms/latest/actions/get-form-metadata?connectionId=$CONNECTION_ID&formId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "formId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/filloutForms/latest/actions/get-form-metadata?${params}`, {
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
| `formId` | string | yes | The form ID to retrieve metadata for. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "calculations": [
        {}
      ],
      "documents": [
        {}
      ],
      "id": "string",
      "name": "Ava Chen",
      "payments": [
        {}
      ],
      "questions": [
        {}
      ],
      "scheduling": [
        {}
      ],
      "tags": [
        "string"
      ],
      "urlParameters": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `calculations` | array<object> | Calculated fields on the form. |
| `documents` | array<object> | Documents configured on the form. |
| `id` | string | Form identifier. |
| `name` | string | Form name. |
| `payments` | array<object> | Payment configuration for the form. |
| `questions` | array<object> | Questions configured on the form. |
| `scheduling` | array<object> | Scheduling configuration for the form. |
| `tags` | array<string> | Tags applied to the form. |
| `urlParameters` | array<object> | URL parameters configured for the form. |

## Native endpoint

Through the native Fillout Forms API, this operation is `GET /forms/:formId` (base URL `https://api.fillout.com/v1/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-form-metadata.md) for the provider-specific parameters and requirements.


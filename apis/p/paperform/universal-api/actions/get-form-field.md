# Paperform: Get Form Field

Retrieves a field from a Paperform form.

```
GET https://connect.mindcloud.co/v1/universal/paperform/latest/actions/get-form-field
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Paperform `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/paperform/latest/actions/get-form-field?connectionId=$CONNECTION_ID&slugOrId=contact-form&fieldKey=first_name" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "slugOrId": "contact-form",
  "fieldKey": "first_name"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/paperform/latest/actions/get-form-field?${params}`, {
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
| `slugOrId` | list<string> | yes | Paperform form slug or numeric ID. Example: `contact-form`. |
| `fieldKey` | list<string> | yes | Paperform field key within the selected form. Example: `first_name`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "description": "string",
      "dropdown": {
        "options": [
          "string"
        ]
      },
      "formSlugOrId": "string",
      "key": "string",
      "required": true,
      "title": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string |  |
| `dropdown` | object |  |
| `dropdown.options` | array<string> |  |
| `formSlugOrId` | string | Form slug or ID used to build the Paperform editor URL. |
| `key` | string |  |
| `required` | boolean |  |
| `title` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Paperform API, this operation is `GET /forms/:slug_or_id/fields/:field_key` (base URL `https://api.paperform.co/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-form-field.md) for the provider-specific parameters and requirements.


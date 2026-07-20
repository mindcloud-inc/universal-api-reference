# Paperform: List Form Fields

Retrieves fields from a Paperform form.

```
GET https://connect.mindcloud.co/v1/universal/paperform/latest/actions/list-form-fields
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Paperform `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/paperform/latest/actions/list-form-fields?connectionId=$CONNECTION_ID&slugOrId=contact-form" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "slugOrId": "contact-form"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/paperform/latest/actions/list-form-fields?${params}`, {
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

## Response

```json
{
  "success": true,
  "data": [
    {
      "description": "string",
      "formSlugOrId": "string",
      "key": "string",
      "options": [
        "string"
      ],
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
| `formSlugOrId` | string | Form slug or ID used to build the Paperform editor URL. |
| `key` | string |  |
| `options` | array<string> |  |
| `required` | boolean |  |
| `title` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Paperform API, this operation is `GET /forms/:slug_or_id/fields` (base URL `https://api.paperform.co/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-form-fields.md) for the provider-specific parameters and requirements.


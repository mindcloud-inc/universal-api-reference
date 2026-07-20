# Wufoo: List Form Fields

Retrieves fields from a specific Wufoo form.

```
GET https://connect.mindcloud.co/v1/universal/wufoo/latest/actions/list-form-fields
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Wufoo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wufoo/latest/actions/list-form-fields?connectionId=$CONNECTION_ID&identifier=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "identifier": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/wufoo/latest/actions/list-form-fields?${params}`, {
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
| `identifier` | string | yes | The Wufoo form hash or URL slug, for example `z18tlglo01kf7h1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "choices": [
        {}
      ],
      "classNames": "Ava Chen",
      "defaultVal": "string",
      "hasOtherField": true,
      "id": "string",
      "instructions": "string",
      "isRequired": "string",
      "page": "string",
      "subFields": [
        {}
      ],
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
| `choices` | array<object> | Available field choices when the field is choice-based. |
| `classNames` | string | Custom CSS classes configured on the field. |
| `defaultVal` | string | Default field value. |
| `hasOtherField` | boolean | Whether the field includes an Other choice. |
| `id` | string | Wufoo field API key. |
| `instructions` | string | Field instructions shown to respondents. |
| `isRequired` | string | Whether the field is required. |
| `page` | string | Page number containing the field. |
| `subFields` | array<object> | Nested field parts such as first and last name. |
| `title` | string | Displayed field label or system field title. |
| `type` | string | Wufoo field type. |

## Native endpoint

Through the native Wufoo API, this operation is `GET /forms/:identifier/fields.json` (base URL `https://{{credentials.subdomain}}.wufoo.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-form-fields.md) for the provider-specific parameters and requirements.


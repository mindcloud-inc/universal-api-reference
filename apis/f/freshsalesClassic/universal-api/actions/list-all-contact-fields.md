# Freshsales Classic: List All Contact Fields

Retrieves contact fields from Freshsales Classic.

```
GET https://connect.mindcloud.co/v1/universal/freshsalesClassic/latest/actions/list-all-contact-fields
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Freshsales Classic `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/freshsalesClassic/latest/actions/list-all-contact-fields?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/freshsalesClassic/latest/actions/list-all-contact-fields?${params}`, {
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
| `include` | string | no | Optional related data to include, for example field_group. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "actionable": true,
      "baseModel": "string",
      "choices": [
        {}
      ],
      "default": true,
      "id": 1,
      "label": "string",
      "name": "Ava Chen",
      "position": 1,
      "quickAddPosition": 1,
      "required": true,
      "type": "string",
      "visible": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `actionable` | boolean | Whether the field can be used in actions. |
| `baseModel` | string | Freshsales base model for the field. |
| `choices` | array<object> | Available option choices for selectable fields. |
| `default` | boolean | Whether the field is a default field. |
| `id` | number | Field ID. |
| `label` | string | Field label. |
| `name` | string | Field API name. |
| `position` | number | Field display position. |
| `quickAddPosition` | number | Quick-add position when defined. |
| `required` | boolean | Whether the field is required. |
| `type` | string | Field input type. |
| `visible` | boolean | Whether the field is visible by default. |

## Native endpoint

Through the native Freshsales Classic API, this operation is `GET /settings/contacts/fields` (base URL `https://{{credentials.bundleAlias}}/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-all-contact-fields.md) for the provider-specific parameters and requirements.


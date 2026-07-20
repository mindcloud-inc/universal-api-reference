# Wufoo: List Report Fields

Retrieves fields from a specific Wufoo report.

```
GET https://connect.mindcloud.co/v1/universal/wufoo/latest/actions/list-report-fields
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Wufoo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wufoo/latest/actions/list-report-fields?connectionId=$CONNECTION_ID&identifier=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "identifier": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/wufoo/latest/actions/list-report-fields?${params}`, {
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
| `identifier` | string | yes | The report hash or identifier whose fields to retrieve. |

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
      "isRequired": 1,
      "page": 1,
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
| `choices` | array<object> | Selectable choices when present. |
| `classNames` | string | Custom class names when present. |
| `defaultVal` | string | Default value when present. |
| `hasOtherField` | boolean | Whether the field supports an Other option. |
| `id` | string | The report field identifier. |
| `instructions` | string | Field instructions when present. |
| `isRequired` | number | Whether the field is required. |
| `page` | number | The page number for the field. |
| `subFields` | array<object> | Sub-fields when present. |
| `title` | string | The report field title. |
| `type` | string | The report field type. |

## Native endpoint

Through the native Wufoo API, this operation is `GET /reports/:identifier/fields.json` (base URL `https://{{credentials.subdomain}}.wufoo.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-report-fields.md) for the provider-specific parameters and requirements.


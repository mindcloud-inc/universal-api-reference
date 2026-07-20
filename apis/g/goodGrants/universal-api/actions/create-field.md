# Good Grants: Create field

Creates a new field in Good Grants.

```
POST https://connect.mindcloud.co/v1/universal/goodGrants/latest/actions/create-field
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Good Grants `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/goodGrants/latest/actions/create-field" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "translated.title.en_US": "string",
  "tab": "string",
  "type": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/goodGrants/latest/actions/create-field', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "translated.title.en_US": "string",
    "tab": "string",
    "type": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `translated.title.en_US` | string | yes | Field title |
| `tab` | string | yes | Tab slug |
| `form` | string | no | Form slug |
| `translated.help_text.en_US` | string | no | Help text |
| `translated.hint_text.en_US` | string | no | Hint text |
| `type` | string | yes | Field type |

## Response

```json
{
  "success": true,
  "data": [
    {
      "applicant_read_access": true,
      "applicant_write_access": true,
      "auto_scoring": 1,
      "categories": [
        "string"
      ],
      "category_count": "string",
      "conditional_field": {},
      "created": "2026-05-07T12:00:00.000Z",
      "file_types": [
        "string"
      ],
      "form": {},
      "help_text": {},
      "hint_text": {},
      "label": {},
      "max_file_size": 1,
      "maximum_characters": 1,
      "maximum_words": 1,
      "minimum_characters": 1,
      "minimum_words": 1,
      "options": [
        {}
      ],
      "order": 1,
      "protection": "string",
      "registration": {},
      "required": true,
      "resource": "string",
      "searchable": true,
      "season": {},
      "slug": "string",
      "tab": {},
      "title": {},
      "type": "string",
      "updated": "2026-05-07T12:00:00.000Z",
      "visibility": [
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
| `applicant_read_access` | boolean |  |
| `applicant_write_access` | boolean |  |
| `auto_scoring` | number |  |
| `categories` | array<string> |  |
| `category_count` | string |  |
| `conditional_field` | object |  |
| `created` | date |  |
| `file_types` | array<string> |  |
| `form` | object |  |
| `help_text` | object |  |
| `hint_text` | object |  |
| `label` | object |  |
| `max_file_size` | number |  |
| `maximum_characters` | number |  |
| `maximum_words` | number |  |
| `minimum_characters` | number |  |
| `minimum_words` | number |  |
| `options` | array<object> |  |
| `order` | number |  |
| `protection` | string |  |
| `registration` | object |  |
| `required` | boolean |  |
| `resource` | string |  |
| `searchable` | boolean |  |
| `season` | object |  |
| `slug` | string |  |
| `tab` | object |  |
| `title` | object |  |
| `type` | string |  |
| `updated` | date |  |
| `visibility` | array<object> |  |

## Native endpoint

Through the native Good Grants API, this operation is `POST field` (base URL `https://api.cr4ce.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-field.md) for the provider-specific parameters and requirements.


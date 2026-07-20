# Content Snare: Create Section

Creates a section in Content Snare.

```
POST https://connect.mindcloud.co/v1/universal/contentSnare/latest/actions/create-section
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Content Snare `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/contentSnare/latest/actions/create-section" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "pageId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/contentSnare/latest/actions/create-section', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "pageId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | no | Section name. If it isn't set then the source template name is used. |
| `pageId` | string | yes | Id of a page where a new section should be added |
| `sourceTemplateId` | string | no | Source section template id (`source_template_id` or `source_template_name` should be set) |
| `sourceTemplateName` | string | no | Source section template name (`source_template_id` or `source_template_name` should be set) |

## Response

```json
{
  "success": true,
  "data": [
    {
      "fields": [
        {
          "additional_fields": [
            {
              "id": "string",
              "sorting_position": 1,
              "text": "string"
            }
          ],
          "answers": [
            {
              "attachment": {
                "byte_size": 1,
                "filename": "Ava Chen",
                "signed_id": "string",
                "url": "https://example.com"
              },
              "field_id": "string",
              "id": "string",
              "link": "https://example.com",
              "rejection_comment": "string",
              "row": [
                {
                  "field_column_id": "string",
                  "text": "string"
                }
              ],
              "sorting_position": 1,
              "status": "string",
              "text": [
                [
                  "string"
                ]
              ]
            }
          ],
          "field_columns": [
            {
              "id": "string",
              "name": "Ava Chen",
              "read_only": true,
              "required": true,
              "sorting_position": 1
            }
          ],
          "field_configuration": {
            "id": "string",
            "settings": {}
          },
          "id": "string",
          "images": [
            {
              "byte_size": 1,
              "filename": "Ava Chen",
              "image": {
                "height": 1,
                "url": "https://example.com",
                "width": 1
              },
              "signed_id": "string",
              "thumbnail": {
                "height": 1,
                "url": "https://example.com",
                "width": 1
              },
              "url": "https://example.com"
            }
          ],
          "instruction_text": "string",
          "internal": true,
          "max_answer_count": 1,
          "min_answer_count": 1,
          "name": "Ava Chen",
          "placeholder": "string",
          "reference_id": "string",
          "rejection_message": {
            "text": "string"
          },
          "repeater_enabled": true,
          "required": true,
          "show_instruction": true,
          "sorting_position": 1,
          "status": "string",
          "sub_type": "string",
          "type": "string",
          "values_flat": "string",
          "values_structured": [
            [
              "string"
            ]
          ],
          "values": [
            [
              "string"
            ]
          ]
        }
      ],
      "id": "string",
      "instruction_text": "string",
      "name": "Ava Chen",
      "reference_id": "string",
      "show_instruction": true,
      "sorting_position": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `fields[].additional_fields[].id` | string |  |
| `fields[].additional_fields[].sorting_position` | number |  |
| `fields[].additional_fields[].text` | string |  |
| `fields[].answers[].attachment.byte_size` | number |  |
| `fields[].answers[].attachment.filename` | string |  |
| `fields[].answers[].attachment.signed_id` | string |  |
| `fields[].answers[].attachment.url` | string |  |
| `fields[].answers[].field_id` | string |  |
| `fields[].answers[].id` | string |  |
| `fields[].answers[].link` | string |  |
| `fields[].answers[].rejection_comment` | string |  |
| `fields[].answers[].row[].field_column_id` | string |  |
| `fields[].answers[].row[].text` | string |  |
| `fields[].answers[].sorting_position` | number |  |
| `fields[].answers[].status` | string |  |
| `fields[].answers[].text[]` | array<string> |  |
| `fields[].field_columns[].id` | string |  |
| `fields[].field_columns[].name` | string |  |
| `fields[].field_columns[].read_only` | boolean |  |
| `fields[].field_columns[].required` | boolean |  |
| `fields[].field_columns[].sorting_position` | number |  |
| `fields[].field_configuration.id` | string |  |
| `fields[].field_configuration.settings` | object |  |
| `fields[].id` | string |  |
| `fields[].images[].byte_size` | number |  |
| `fields[].images[].filename` | string |  |
| `fields[].images[].image.height` | number |  |
| `fields[].images[].image.url` | string |  |
| `fields[].images[].image.width` | number |  |
| `fields[].images[].signed_id` | string |  |
| `fields[].images[].thumbnail.height` | number |  |
| `fields[].images[].thumbnail.url` | string |  |
| `fields[].images[].thumbnail.width` | number |  |
| `fields[].images[].url` | string |  |
| `fields[].instruction_text` | string |  |
| `fields[].internal` | boolean | A boolean value indicating whether the field is visible only to team members and hidden from clients |
| `fields[].max_answer_count` | number |  |
| `fields[].min_answer_count` | number |  |
| `fields[].name` | string |  |
| `fields[].placeholder` | string |  |
| `fields[].reference_id` | string | A reference ID is a unique identifier that remains consistent across all instances of a field, whether in multiple requests or within repeated sections of the same request |
| `fields[].rejection_message.text` | string |  |
| `fields[].repeater_enabled` | boolean |  |
| `fields[].required` | boolean |  |
| `fields[].show_instruction` | boolean |  |
| `fields[].sorting_position` | number |  |
| `fields[].status` | string |  |
| `fields[].sub_type` | string |  |
| `fields[].type` | string |  |
| `fields[].values_flat` | string |  |
| `fields[].values_structured[]` | array<string> |  |
| `fields[].values[]` | array<string> |  |
| `id` | string |  |
| `instruction_text` | string |  |
| `name` | string |  |
| `reference_id` | string | A reference ID is an identifier, unique within a page, that remains consistent across all instances of a section, whether in multiple requests or within duplicated pages of the same request |
| `show_instruction` | boolean |  |
| `sorting_position` | number |  |

## Native endpoint

Through the native Content Snare API, this operation is `POST /partner_api/v1/sections` (base URL `https://api.contentsnare.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-section.md) for the provider-specific parameters and requirements.


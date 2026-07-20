# Content Snare: Create Page

Creates a page in Content Snare.

```
POST https://connect.mindcloud.co/v1/universal/contentSnare/latest/actions/create-page
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Content Snare `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/contentSnare/latest/actions/create-page" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "requestId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/contentSnare/latest/actions/create-page', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "requestId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | no | Page name. If it isn't set then the source template name is used. |
| `requestId` | string | yes | Id of a request where a new page should be added |
| `sourceTemplateId` | string | no | Source page template id (`source_template_id` or `source_template_name` should be set) |
| `sourceTemplateName` | string | no | Source page template name (`source_template_id` or `source_template_name` should be set) |

## Response

```json
{
  "success": true,
  "data": [
    {
      "approved_fields_count": 1,
      "done_fields_count": 1,
      "fields_count": 1,
      "id": "string",
      "instruction_text": "string",
      "is_approved": true,
      "is_done": true,
      "name": "Ava Chen",
      "redo_fields_count": 1,
      "reference_id": "string",
      "sections": [
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
| `approved_fields_count` | number |  |
| `done_fields_count` | number |  |
| `fields_count` | number |  |
| `id` | string |  |
| `instruction_text` | string |  |
| `is_approved` | boolean |  |
| `is_done` | boolean |  |
| `name` | string |  |
| `redo_fields_count` | number |  |
| `reference_id` | string | A reference ID is an identifier, unique within a request, that remains consistent across all instances of a page in multiple requests and request templates |
| `sections[].fields[].additional_fields[].id` | string |  |
| `sections[].fields[].additional_fields[].sorting_position` | number |  |
| `sections[].fields[].additional_fields[].text` | string |  |
| `sections[].fields[].answers[].attachment.byte_size` | number |  |
| `sections[].fields[].answers[].attachment.filename` | string |  |
| `sections[].fields[].answers[].attachment.signed_id` | string |  |
| `sections[].fields[].answers[].attachment.url` | string |  |
| `sections[].fields[].answers[].field_id` | string |  |
| `sections[].fields[].answers[].id` | string |  |
| `sections[].fields[].answers[].link` | string |  |
| `sections[].fields[].answers[].rejection_comment` | string |  |
| `sections[].fields[].answers[].row[].field_column_id` | string |  |
| `sections[].fields[].answers[].row[].text` | string |  |
| `sections[].fields[].answers[].sorting_position` | number |  |
| `sections[].fields[].answers[].status` | string |  |
| `sections[].fields[].answers[].text[]` | array<string> |  |
| `sections[].fields[].field_columns[].id` | string |  |
| `sections[].fields[].field_columns[].name` | string |  |
| `sections[].fields[].field_columns[].read_only` | boolean |  |
| `sections[].fields[].field_columns[].required` | boolean |  |
| `sections[].fields[].field_columns[].sorting_position` | number |  |
| `sections[].fields[].field_configuration.id` | string |  |
| `sections[].fields[].field_configuration.settings` | object |  |
| `sections[].fields[].id` | string |  |
| `sections[].fields[].images[].byte_size` | number |  |
| `sections[].fields[].images[].filename` | string |  |
| `sections[].fields[].images[].image.height` | number |  |
| `sections[].fields[].images[].image.url` | string |  |
| `sections[].fields[].images[].image.width` | number |  |
| `sections[].fields[].images[].signed_id` | string |  |
| `sections[].fields[].images[].thumbnail.height` | number |  |
| `sections[].fields[].images[].thumbnail.url` | string |  |
| `sections[].fields[].images[].thumbnail.width` | number |  |
| `sections[].fields[].images[].url` | string |  |
| `sections[].fields[].instruction_text` | string |  |
| `sections[].fields[].internal` | boolean | A boolean value indicating whether the field is visible only to team members and hidden from clients |
| `sections[].fields[].max_answer_count` | number |  |
| `sections[].fields[].min_answer_count` | number |  |
| `sections[].fields[].name` | string |  |
| `sections[].fields[].placeholder` | string |  |
| `sections[].fields[].reference_id` | string | A reference ID is a unique identifier that remains consistent across all instances of a field, whether in multiple requests or within repeated sections of the same request |
| `sections[].fields[].rejection_message.text` | string |  |
| `sections[].fields[].repeater_enabled` | boolean |  |
| `sections[].fields[].required` | boolean |  |
| `sections[].fields[].show_instruction` | boolean |  |
| `sections[].fields[].sorting_position` | number |  |
| `sections[].fields[].status` | string |  |
| `sections[].fields[].sub_type` | string |  |
| `sections[].fields[].type` | string |  |
| `sections[].fields[].values_flat` | string |  |
| `sections[].fields[].values_structured[]` | array<string> |  |
| `sections[].fields[].values[]` | array<string> |  |
| `sections[].id` | string |  |
| `sections[].instruction_text` | string |  |
| `sections[].name` | string |  |
| `sections[].reference_id` | string | A reference ID is an identifier, unique within a page, that remains consistent across all instances of a section, whether in multiple requests or within duplicated pages of the same request |
| `sections[].show_instruction` | boolean |  |
| `sections[].sorting_position` | number |  |
| `show_instruction` | boolean |  |
| `sorting_position` | number |  |

## Native endpoint

Through the native Content Snare API, this operation is `POST /partner_api/v1/pages` (base URL `https://api.contentsnare.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-page.md) for the provider-specific parameters and requirements.


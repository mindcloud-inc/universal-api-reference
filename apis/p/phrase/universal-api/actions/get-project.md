# Phrase: Get Project

Retrieves a single project from Phrase.

```
GET https://connect.mindcloud.co/v1/universal/phrase/latest/actions/get-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Phrase `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/phrase/latest/actions/get-project?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/phrase/latest/actions/get-project?${params}`, {
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
| `id` | string | yes | Phrase project id to fetch. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "account": {},
      "autotranslate_check_new_locales": true,
      "autotranslate_check_new_translation_keys": true,
      "autotranslate_check_new_uploads": true,
      "autotranslate_enabled": true,
      "autotranslate_mark_as_unverified": true,
      "autotranslate_use_machine_translation": true,
      "autotranslate_use_translation_memory": true,
      "cldr_version": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "default_encoding": "string",
      "enable_all_data_type_translation_keys_for_translators": true,
      "enable_branching": true,
      "enable_icu_message_format": true,
      "id": "string",
      "job_locking_enabled": true,
      "machine_translation_enabled": true,
      "main_format": "string",
      "media": "string",
      "name": "Ava Chen",
      "placeholder_styles": [
        "string"
      ],
      "point_of_contact": {},
      "project_image_url": "https://example.com",
      "protect_master_branch": true,
      "shares_translation_memory": true,
      "slug": "string",
      "space": {},
      "updated_at": "2026-05-07T12:00:00.000Z",
      "zero_plural_form_enabled": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `account` | object |  |
| `autotranslate_check_new_locales` | boolean |  |
| `autotranslate_check_new_translation_keys` | boolean |  |
| `autotranslate_check_new_uploads` | boolean |  |
| `autotranslate_enabled` | boolean |  |
| `autotranslate_mark_as_unverified` | boolean |  |
| `autotranslate_use_machine_translation` | boolean |  |
| `autotranslate_use_translation_memory` | boolean |  |
| `cldr_version` | string |  |
| `created_at` | date |  |
| `default_encoding` | string |  |
| `enable_all_data_type_translation_keys_for_translators` | boolean |  |
| `enable_branching` | boolean |  |
| `enable_icu_message_format` | boolean |  |
| `id` | string |  |
| `job_locking_enabled` | boolean |  |
| `machine_translation_enabled` | boolean |  |
| `main_format` | string |  |
| `media` | string |  |
| `name` | string |  |
| `placeholder_styles` | array<string> |  |
| `point_of_contact` | object |  |
| `project_image_url` | string |  |
| `protect_master_branch` | boolean |  |
| `shares_translation_memory` | boolean |  |
| `slug` | string |  |
| `space` | object |  |
| `updated_at` | date |  |
| `zero_plural_form_enabled` | boolean |  |

## Native endpoint

Through the native Phrase API, this operation is `GET /projects/{id}` (base URL `https://api.phrase.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-project.md) for the provider-specific parameters and requirements.


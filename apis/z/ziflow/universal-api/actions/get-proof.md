# Ziflow: Get Proof

Retrieves a proof from Ziflow by ID.

```
GET https://connect.mindcloud.co/v1/universal/ziflow/latest/actions/get-proof
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ziflow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ziflow/latest/actions/get-proof?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ziflow/latest/actions/get-proof?${params}`, {
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
| `id` | string | yes | The proof ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "allow_source_download": true,
      "archived": true,
      "brief": {
        "text": "string"
      },
      "created_at": "string",
      "custom_properties": [
        {
          "id": "string",
          "name": "Ava Chen",
          "properties": [
            {
              "id": "string",
              "name": "Ava Chen",
              "value": "string",
              "value_enum": [
                {
                  "id": "string",
                  "value": "string"
                }
              ],
              "value_user": {
                "email": "ava@example.com"
              }
            }
          ]
        }
      ],
      "decision_status": "string",
      "decision_status_label": "string",
      "download_link": "https://example.com",
      "email_branding": {
        "custom_button": {
          "enabled": true,
          "label": "ava@example.com",
          "url": "ava@example.com"
        },
        "hide_open_proof_button": true,
        "replace_all_proof_urls": "ava@example.com"
      },
      "folder": {
        "archived": true,
        "folder_link": "https://example.com",
        "folder_path": [
          "string"
        ],
        "id": "string",
        "name": "Ava Chen",
        "owner": {
          "blocked": true,
          "company": "string",
          "email": "ava@example.com",
          "first_name": "Ava",
          "id": "string",
          "language": "string",
          "last_name": "Chen",
          "phone": "string",
          "proofing_defaults": {
            "comment": true,
            "decision": true,
            "manage": true,
            "share": true,
            "view": true
          },
          "roles": [
            "string"
          ],
          "timezone": "string",
          "type": "string",
          "verified": true
        },
        "parent_folder_id": "string",
        "private": true
      },
      "id": "string",
      "image_link": "https://example.com",
      "integration_properties": [
        {
          "application_key": "string",
          "application_name": "Ava Chen",
          "groups": [
            {
              "id": "string",
              "key": "string",
              "labels": [
                "string"
              ],
              "name": "Ava Chen",
              "properties": [
                {
                  "key": "string",
                  "name": "Ava Chen",
                  "value": "string"
                }
              ]
            }
          ]
        }
      ],
      "lock_on_decisions": true,
      "locked": true,
      "minor_version": true,
      "name": "Ava Chen",
      "owner": {
        "blocked": true
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `allow_source_download` | boolean |  |
| `archived` | boolean |  |
| `brief.text` | string |  |
| `created_at` | string |  |
| `custom_properties[].id` | string |  |
| `custom_properties[].name` | string |  |
| `custom_properties[].properties[].id` | string |  |
| `custom_properties[].properties[].name` | string |  |
| `custom_properties[].properties[].value` | string |  |
| `custom_properties[].properties[].value_enum[].id` | string |  |
| `custom_properties[].properties[].value_enum[].value` | string |  |
| `custom_properties[].properties[].value_user.email` | string |  |
| `decision_status` | string |  |
| `decision_status_label` | string |  |
| `download_link` | string |  |
| `email_branding.custom_button.enabled` | boolean |  |
| `email_branding.custom_button.label` | string |  |
| `email_branding.custom_button.url` | string |  |
| `email_branding.hide_open_proof_button` | boolean |  |
| `email_branding.replace_all_proof_urls` | string |  |
| `folder.archived` | boolean |  |
| `folder.folder_link` | string |  |
| `folder.folder_path[]` | string |  |
| `folder.id` | string |  |
| `folder.name` | string |  |
| `folder.owner.blocked` | boolean |  |
| `folder.owner.company` | string |  |
| `folder.owner.email` | string |  |
| `folder.owner.first_name` | string |  |
| `folder.owner.id` | string |  |
| `folder.owner.language` | string |  |
| `folder.owner.last_name` | string |  |
| `folder.owner.phone` | string |  |
| `folder.owner.proofing_defaults.comment` | boolean |  |
| `folder.owner.proofing_defaults.decision` | boolean |  |
| `folder.owner.proofing_defaults.manage` | boolean |  |
| `folder.owner.proofing_defaults.share` | boolean |  |
| `folder.owner.proofing_defaults.view` | boolean |  |
| `folder.owner.roles[]` | string |  |
| `folder.owner.timezone` | string |  |
| `folder.owner.type` | string |  |
| `folder.owner.verified` | boolean |  |
| `folder.parent_folder_id` | string |  |
| `folder.private` | boolean |  |
| `id` | string |  |
| `image_link` | string |  |
| `integration_properties[].application_key` | string |  |
| `integration_properties[].application_name` | string |  |
| `integration_properties[].groups[].id` | string |  |
| `integration_properties[].groups[].key` | string |  |
| `integration_properties[].groups[].labels[]` | string |  |
| `integration_properties[].groups[].name` | string |  |
| `integration_properties[].groups[].properties[].key` | string |  |
| `integration_properties[].groups[].properties[].name` | string |  |
| `integration_properties[].groups[].properties[].value` | string |  |
| `lock_on_decisions` | boolean |  |
| `locked` | boolean |  |
| `minor_version` | boolean |  |
| `name` | string |  |
| `owner.blocked` | boolean |  |

## Native endpoint

Through the native Ziflow API, this operation is `GET /proofs/:id` (base URL `https://api.ziflow.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-proof.md) for the provider-specific parameters and requirements.


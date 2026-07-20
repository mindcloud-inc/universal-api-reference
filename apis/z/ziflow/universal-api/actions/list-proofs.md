# Ziflow: List Proofs

Retrieves proofs from your Ziflow account.

```
GET https://connect.mindcloud.co/v1/universal/ziflow/latest/actions/list-proofs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ziflow `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ziflow/latest/actions/list-proofs?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ziflow/latest/actions/list-proofs?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1,
      "has_more": true,
      "page": 1,
      "proofs": [
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
          "locked": true
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number |  |
| `has_more` | boolean |  |
| `page` | number |  |
| `proofs[].allow_source_download` | boolean |  |
| `proofs[].archived` | boolean |  |
| `proofs[].brief.text` | string |  |
| `proofs[].created_at` | string |  |
| `proofs[].custom_properties[].id` | string |  |
| `proofs[].custom_properties[].name` | string |  |
| `proofs[].custom_properties[].properties[].id` | string |  |
| `proofs[].custom_properties[].properties[].name` | string |  |
| `proofs[].custom_properties[].properties[].value` | string |  |
| `proofs[].custom_properties[].properties[].value_enum[].id` | string |  |
| `proofs[].custom_properties[].properties[].value_enum[].value` | string |  |
| `proofs[].custom_properties[].properties[].value_user.email` | string |  |
| `proofs[].decision_status` | string |  |
| `proofs[].decision_status_label` | string |  |
| `proofs[].download_link` | string |  |
| `proofs[].email_branding.custom_button.enabled` | boolean |  |
| `proofs[].email_branding.custom_button.label` | string |  |
| `proofs[].email_branding.custom_button.url` | string |  |
| `proofs[].email_branding.hide_open_proof_button` | boolean |  |
| `proofs[].email_branding.replace_all_proof_urls` | string |  |
| `proofs[].folder.archived` | boolean |  |
| `proofs[].folder.folder_link` | string |  |
| `proofs[].folder.folder_path[]` | string |  |
| `proofs[].folder.id` | string |  |
| `proofs[].folder.name` | string |  |
| `proofs[].folder.owner.blocked` | boolean |  |
| `proofs[].folder.owner.company` | string |  |
| `proofs[].folder.owner.email` | string |  |
| `proofs[].folder.owner.first_name` | string |  |
| `proofs[].folder.owner.id` | string |  |
| `proofs[].folder.owner.language` | string |  |
| `proofs[].folder.owner.last_name` | string |  |
| `proofs[].folder.owner.phone` | string |  |
| `proofs[].folder.owner.proofing_defaults.comment` | boolean |  |
| `proofs[].folder.owner.proofing_defaults.decision` | boolean |  |
| `proofs[].folder.owner.proofing_defaults.manage` | boolean |  |
| `proofs[].folder.owner.proofing_defaults.share` | boolean |  |
| `proofs[].folder.owner.proofing_defaults.view` | boolean |  |
| `proofs[].folder.owner.roles[]` | string |  |
| `proofs[].folder.owner.timezone` | string |  |
| `proofs[].folder.owner.type` | string |  |
| `proofs[].folder.owner.verified` | boolean |  |
| `proofs[].folder.parent_folder_id` | string |  |
| `proofs[].folder.private` | boolean |  |
| `proofs[].id` | string |  |
| `proofs[].image_link` | string |  |
| `proofs[].integration_properties[].application_key` | string |  |
| `proofs[].integration_properties[].application_name` | string |  |
| `proofs[].integration_properties[].groups[].id` | string |  |
| `proofs[].integration_properties[].groups[].key` | string |  |
| `proofs[].integration_properties[].groups[].labels[]` | string |  |
| `proofs[].integration_properties[].groups[].name` | string |  |
| `proofs[].integration_properties[].groups[].properties[].key` | string |  |
| `proofs[].integration_properties[].groups[].properties[].name` | string |  |
| `proofs[].integration_properties[].groups[].properties[].value` | string |  |
| `proofs[].lock_on_decisions` | boolean |  |
| `proofs[].locked` | boolean |  |

## Native endpoint

Through the native Ziflow API, this operation is `GET /proofs` (base URL `https://api.ziflow.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-proofs.md) for the provider-specific parameters and requirements.


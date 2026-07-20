# Ziflow: Get Folder

Retrieves subfolders in a Ziflow folder.

```
GET https://connect.mindcloud.co/v1/universal/ziflow/latest/actions/get-folder
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ziflow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ziflow/latest/actions/get-folder?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ziflow/latest/actions/get-folder?${params}`, {
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
| `id` | string | yes | The folder ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
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
          "notification": "string",
          "share": true,
          "view": true
        },
        "roles": [
          "string"
        ],
        "tenant": {
          "company_name": "Ava Chen",
          "subdomain": "string",
          "tenant_id": "string"
        },
        "timezone": "string",
        "type": "string",
        "verified": true
      },
      "parent_folder_id": "string",
      "private": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archived` | boolean |  |
| `folder_link` | string |  |
| `folder_path[]` | string |  |
| `id` | string |  |
| `name` | string |  |
| `owner.blocked` | boolean |  |
| `owner.company` | string |  |
| `owner.email` | string |  |
| `owner.first_name` | string |  |
| `owner.id` | string |  |
| `owner.language` | string |  |
| `owner.last_name` | string |  |
| `owner.phone` | string |  |
| `owner.proofing_defaults.comment` | boolean |  |
| `owner.proofing_defaults.decision` | boolean |  |
| `owner.proofing_defaults.manage` | boolean |  |
| `owner.proofing_defaults.notification` | string |  |
| `owner.proofing_defaults.share` | boolean |  |
| `owner.proofing_defaults.view` | boolean |  |
| `owner.roles[]` | string |  |
| `owner.tenant.company_name` | string |  |
| `owner.tenant.subdomain` | string |  |
| `owner.tenant.tenant_id` | string |  |
| `owner.timezone` | string |  |
| `owner.type` | string |  |
| `owner.verified` | boolean |  |
| `parent_folder_id` | string |  |
| `private` | boolean |  |

## Native endpoint

Through the native Ziflow API, this operation is `GET /folders/:id` (base URL `https://api.ziflow.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-folder.md) for the provider-specific parameters and requirements.


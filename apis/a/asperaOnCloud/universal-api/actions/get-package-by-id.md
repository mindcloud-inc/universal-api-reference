# Aspera on Cloud: Get Package

Retrieves a package from Aspera on Cloud.

```
GET https://connect.mindcloud.co/v1/universal/asperaOnCloud/latest/actions/get-package-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Aspera on Cloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/asperaOnCloud/latest/actions/get-package-by-id?connectionId=$CONNECTION_ID&id=pkg_123" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "pkg_123"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/asperaOnCloud/latest/actions/get-package-by-id?${params}`, {
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
| `id` | string | yes | ID of the package. Example: `pkg_123`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active_download_count": 1,
      "archived": true,
      "average_rate": 1,
      "bcc": true,
      "bcc_recipients": {
        "id": "string",
        "type": "string"
      },
      "bytes_transferred": 1,
      "complete": true,
      "completed_at": "string",
      "content_expires_at": "string",
      "content_retention_duration": 1,
      "contents_file_id": "string",
      "created_at": "string",
      "delete_after_download": true,
      "delete_package_content_after_download_duration": 1,
      "deleted": true,
      "deleted_after_download": true,
      "deleted_at": "string",
      "deleted_by_admin": true,
      "deleted_by_user_id": 1,
      "download_notification_recipients": {
        "id": "string",
        "type": "string"
      },
      "draft": true,
      "draft_expires_at": "string",
      "encryption_at_rest": true,
      "expiration_reason": "string",
      "expired": true,
      "expired_at": "string",
      "failed": true,
      "failed_download_count": 1,
      "file_count": 1,
      "file_count_from_disk": true,
      "file_id": "string",
      "files_completed": 1,
      "files_expected": 1,
      "folder_count": 1,
      "folders_completed": 1,
      "folders_expected": 1,
      "full_download_count": 1,
      "has_content": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active_download_count` | number |  |
| `archived` | boolean |  |
| `average_rate` | number |  |
| `bcc` | boolean |  |
| `bcc_recipients.id` | string |  |
| `bcc_recipients.type` | string |  |
| `bytes_transferred` | number |  |
| `complete` | boolean |  |
| `completed_at` | string |  |
| `content_expires_at` | string |  |
| `content_retention_duration` | number |  |
| `contents_file_id` | string |  |
| `created_at` | string |  |
| `delete_after_download` | boolean |  |
| `delete_package_content_after_download_duration` | number |  |
| `deleted` | boolean |  |
| `deleted_after_download` | boolean |  |
| `deleted_at` | string |  |
| `deleted_by_admin` | boolean |  |
| `deleted_by_user_id` | number |  |
| `download_notification_recipients.id` | string |  |
| `download_notification_recipients.type` | string |  |
| `draft` | boolean |  |
| `draft_expires_at` | string |  |
| `encryption_at_rest` | boolean |  |
| `expiration_reason` | string |  |
| `expired` | boolean |  |
| `expired_at` | string |  |
| `failed` | boolean |  |
| `failed_download_count` | number |  |
| `file_count` | number |  |
| `file_count_from_disk` | boolean |  |
| `file_id` | string |  |
| `files_completed` | number |  |
| `files_expected` | number |  |
| `folder_count` | number |  |
| `folders_completed` | number |  |
| `folders_expected` | number |  |
| `full_download_count` | number |  |
| `has_content` | boolean |  |

## Native endpoint

Through the native Aspera on Cloud API, this operation is `GET /v1/packages/{id}` (base URL `https://api.ibmaspera.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-package-by-id.md) for the provider-specific parameters and requirements.


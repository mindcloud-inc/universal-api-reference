# Aspera on Cloud Universal API Examples

These examples use the MindCloud API key and Aspera on Cloud connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Packages

Retrieves packages from Aspera on Cloud.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/asperaOnCloud/latest/actions/get-packages?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/asperaOnCloud/latest/actions/get-packages?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

Example response:

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

See the full [List Packages action reference](actions/get-packages.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/asperaOnCloud/latest/actions/get-packages).

## Create Shared Inbox

Creates a new shared inbox in Aspera on Cloud.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/asperaOnCloud/latest/actions/add-dropbox" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/asperaOnCloud/latest/actions/add-dropbox', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "content_retention_duration": 1,
      "custom_notification_list_enabled": true,
      "delete_package_content_after_download_duration": 1,
      "description": "string",
      "draft_expiration_duration": 1,
      "dropbox_notification_recipients": {
        "id": "string",
        "type": "string"
      },
      "effective_content_retention_duration": 1,
      "effective_delete_package_content_after_download_duration": 1,
      "email_notification_settings": {
        "dropbox_invitation": true,
        "file_shared": true,
        "invitation_to_send_to_me": true,
        "package_contents_deleted": true,
        "package_downloaded": true,
        "package_expired": true,
        "package_failed": true,
        "package_recalled": true,
        "package_received": true,
        "package_resent": true,
        "package_sent": true,
        "package_uploaded": true
      },
      "enable_external_email_templates": true,
      "id": "string",
      "image_url": "https://example.com",
      "inherit_email_notification_settings": true,
      "inherit_email_templates": true,
      "inherit_workspace_expiration_settings": true,
      "instructions": "string",
      "metadata_schema": {
        "choices": [
          "string"
        ],
        "default_values": [
          "string"
        ],
        "illegal_characters": "string",
        "input_type": "string",
        "max_length": "string",
        "name": "Ava Chen",
        "required": true
      },
      "name": "Ava Chen",
      "package_name_and_message_validation_schema": {
        "field_name": "Ava Chen",
        "illegal_characters": "Ava Chen",
        "max_length": "Ava Chen"
      },
      "personalized_urls_enabled": true
    }
  ],
  "meta": {}
}
```

See the full [Create Shared Inbox action reference](actions/add-dropbox.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/asperaOnCloud/latest/actions/add-dropbox).

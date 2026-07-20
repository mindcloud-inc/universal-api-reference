# Aspera on Cloud: Create Workspace

Creates a new workspace in Aspera on Cloud.

```
POST https://connect.mindcloud.co/v1/universal/asperaOnCloud/latest/actions/add-workspace
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Aspera on Cloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/asperaOnCloud/latest/actions/add-workspace" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/asperaOnCloud/latest/actions/add-workspace', {
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



## Response

```json
{
  "success": true,
  "data": [
    {
      "allow_package_level_expirations": true,
      "can_invite_by_email": true,
      "collaboration_settings_editable_by_managers": true,
      "collaboration_whitelist_enabled": true,
      "collaboration_with_emails_allowed": true,
      "content_retention_duration": 1,
      "created_at": "string",
      "default_ear_setting": true,
      "delete_package_content_after_download_duration": 1,
      "description": "string",
      "draft_expiration_duration": 1,
      "effective_default_ear_setting": true,
      "effective_storage_allowed": true,
      "email_footer": "ava@example.com",
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
      "enable_external_notifications": true,
      "event_reporting_headers": "string",
      "event_reporting_uri": "string",
      "external_package_authentication_required": true,
      "external_package_sending_allowed": true,
      "external_package_sending_allowed_by_managers": true,
      "external_sharing_allowed": true,
      "external_sharing_allowed_by_managers": true,
      "group_id": 1,
      "home_container_file_id": "string",
      "home_file_id": 1,
      "home_node_id": 1,
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `allow_package_level_expirations` | boolean |  |
| `can_invite_by_email` | boolean |  |
| `collaboration_settings_editable_by_managers` | boolean |  |
| `collaboration_whitelist_enabled` | boolean |  |
| `collaboration_with_emails_allowed` | boolean |  |
| `content_retention_duration` | number |  |
| `created_at` | string |  |
| `default_ear_setting` | boolean |  |
| `delete_package_content_after_download_duration` | number |  |
| `description` | string |  |
| `draft_expiration_duration` | number |  |
| `effective_default_ear_setting` | boolean |  |
| `effective_storage_allowed` | boolean |  |
| `email_footer` | string |  |
| `email_notification_settings.dropbox_invitation` | boolean |  |
| `email_notification_settings.file_shared` | boolean |  |
| `email_notification_settings.invitation_to_send_to_me` | boolean |  |
| `email_notification_settings.package_contents_deleted` | boolean |  |
| `email_notification_settings.package_downloaded` | boolean |  |
| `email_notification_settings.package_expired` | boolean |  |
| `email_notification_settings.package_failed` | boolean |  |
| `email_notification_settings.package_recalled` | boolean |  |
| `email_notification_settings.package_received` | boolean |  |
| `email_notification_settings.package_resent` | boolean |  |
| `email_notification_settings.package_sent` | boolean |  |
| `email_notification_settings.package_uploaded` | boolean |  |
| `enable_external_email_templates` | boolean |  |
| `enable_external_notifications` | boolean |  |
| `event_reporting_headers` | string |  |
| `event_reporting_uri` | string |  |
| `external_package_authentication_required` | boolean |  |
| `external_package_sending_allowed` | boolean |  |
| `external_package_sending_allowed_by_managers` | boolean |  |
| `external_sharing_allowed` | boolean |  |
| `external_sharing_allowed_by_managers` | boolean |  |
| `group_id` | number |  |
| `home_container_file_id` | string |  |
| `home_file_id` | number |  |
| `home_node_id` | number |  |
| `id` | string |  |

## Native endpoint

Through the native Aspera on Cloud API, this operation is `POST /v1/workspaces` (base URL `https://api.ibmaspera.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-workspace.md) for the provider-specific parameters and requirements.


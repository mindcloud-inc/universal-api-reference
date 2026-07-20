# Aspera on Cloud: Create Shared Inbox

Creates a new shared inbox in Aspera on Cloud.

```
POST https://connect.mindcloud.co/v1/universal/asperaOnCloud/latest/actions/add-dropbox
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Aspera on Cloud `connectionId` ([setup](../authentication.md)).

## Example request

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



## Response

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

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `content_retention_duration` | number |  |
| `custom_notification_list_enabled` | boolean |  |
| `delete_package_content_after_download_duration` | number |  |
| `description` | string |  |
| `draft_expiration_duration` | number |  |
| `dropbox_notification_recipients.id` | string |  |
| `dropbox_notification_recipients.type` | string |  |
| `effective_content_retention_duration` | number |  |
| `effective_delete_package_content_after_download_duration` | number |  |
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
| `id` | string |  |
| `image_url` | string |  |
| `inherit_email_notification_settings` | boolean |  |
| `inherit_email_templates` | boolean |  |
| `inherit_workspace_expiration_settings` | boolean |  |
| `instructions` | string |  |
| `metadata_schema.choices` | array<string> |  |
| `metadata_schema.default_values` | array<string> |  |
| `metadata_schema.illegal_characters` | string |  |
| `metadata_schema.input_type` | string |  |
| `metadata_schema.max_length` | string |  |
| `metadata_schema.name` | string |  |
| `metadata_schema.required` | boolean |  |
| `name` | string |  |
| `package_name_and_message_validation_schema.field_name` | string |  |
| `package_name_and_message_validation_schema.illegal_characters` | string |  |
| `package_name_and_message_validation_schema.max_length` | string |  |
| `personalized_urls_enabled` | boolean |  |

## Native endpoint

Through the native Aspera on Cloud API, this operation is `POST /v1/dropboxes` (base URL `https://api.ibmaspera.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-dropbox.md) for the provider-specific parameters and requirements.


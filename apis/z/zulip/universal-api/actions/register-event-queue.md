# Zulip: Register Event Queue

Registers a real-time event queue in Zulip.

```
POST https://connect.mindcloud.co/v1/universal/zulip/latest/actions/register-event-queue
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zulip `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zulip/latest/actions/register-event-queue" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zulip/latest/actions/register-event-queue', {
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
      "alert_words": [
        "string"
      ],
      "avatar_source": "string",
      "avatar_url": "https://example.com",
      "avatar_url_medium": "https://example.com",
      "can_create_private_streams": true,
      "can_create_public_streams": true,
      "can_create_streams": true,
      "can_create_web_public_streams": true,
      "can_invite_others_to_realm": true,
      "channel_folders": [
        "string"
      ],
      "cross_realm_bots": [
        {}
      ],
      "custom_profile_field_types": {},
      "custom_profile_fields": [
        "string"
      ],
      "delivery_email": "ava@example.com",
      "development_environment": true,
      "devices": {},
      "drafts": [
        "string"
      ],
      "email": "ava@example.com",
      "event_queue_longpoll_timeout_seconds": 1,
      "full_name": "Ava Chen",
      "gif_rating_policy_options": {},
      "giphy_api_key": "string",
      "has_zoom_token": true,
      "is_admin": true,
      "is_guest": true,
      "is_moderator": true,
      "is_owner": true,
      "jitsi_server_url": "https://example.com",
      "last_event_id": 1,
      "max_avatar_file_size_mib": 1,
      "max_bulk_new_subscription_messages": 1,
      "max_channel_folder_description_length": 1,
      "max_channel_folder_name_length": 1,
      "max_file_upload_size_mib": 1,
      "max_icon_file_size_mib": 1,
      "max_logo_file_size_mib": 1,
      "max_message_id": 1,
      "max_message_length": 1,
      "max_reminder_note_length": 1,
      "max_stream_description_length": 1,
      "max_stream_name_length": 1,
      "max_topic_length": 1,
      "msg": "string",
      "muted_topics": [
        "string"
      ],
      "muted_users": [
        "string"
      ],
      "navigation_tour_video_url": "https://example.com",
      "navigation_views": [
        "string"
      ],
      "never_subscribed": [
        {}
      ],
      "onboarding_steps": [
        {}
      ],
      "password_max_length": 1,
      "password_min_guesses": 1,
      "password_min_length": 1,
      "presence_last_update_id": 1,
      "presences": {},
      "queue_id": "string",
      "realm_allow_edit_history": true,
      "realm_allow_message_editing": true,
      "realm_authentication_methods": {},
      "realm_available_video_chat_providers": {},
      "realm_avatar_changes_disabled": true,
      "realm_billing": {},
      "realm_bot_domain": "string",
      "realm_bots": [
        "string"
      ],
      "realm_can_access_all_users_group": 1,
      "realm_can_add_custom_emoji_group": 1,
      "realm_can_add_subscribers_group": 1,
      "realm_can_create_bots_group": 1,
      "realm_can_create_groups": 1,
      "realm_can_create_private_channel_group": 1,
      "realm_can_create_public_channel_group": 1,
      "realm_can_create_web_public_channel_group": 1,
      "realm_can_create_write_only_bots_group": 1,
      "realm_can_delete_any_message_group": 1,
      "realm_can_delete_own_message_group": 1,
      "realm_can_invite_users_group": 1,
      "realm_can_manage_all_groups": 1,
      "realm_can_manage_billing_group": 1,
      "realm_can_mention_many_users_group": 1,
      "realm_can_move_messages_between_channels_group": 1,
      "realm_can_move_messages_between_topics_group": 1,
      "realm_can_resolve_topics_group": 1,
      "realm_can_set_delete_message_policy_group": 1,
      "realm_can_set_topics_policy_group": 1,
      "realm_can_summarize_topics_group": 1,
      "realm_create_multiuse_invite_group": 1,
      "realm_create_private_stream_policy": 1,
      "realm_create_public_stream_policy": 1,
      "realm_create_web_public_stream_policy": 1,
      "realm_date_created": 1,
      "realm_default_avatar_source": "string",
      "realm_default_code_block_language": "string",
      "realm_default_external_accounts": {},
      "realm_default_language": "string",
      "realm_default_stream_groups": [
        "string"
      ],
      "realm_default_streams": [
        1
      ],
      "realm_description": "string",
      "realm_digest_emails_enabled": true,
      "realm_digest_weekday": 1,
      "realm_direct_message_initiator_group": 1,
      "realm_direct_message_permission_group": 1,
      "realm_disallow_disposable_email_addresses": true,
      "realm_domains": [
        "string"
      ],
      "realm_email_auth_enabled": true,
      "realm_email_changes_disabled": true,
      "realm_emails_restricted_to_domains": true,
      "realm_embedded_bots": [
        {}
      ],
      "realm_emoji": {},
      "realm_empty_topic_display_name": "Ava Chen",
      "realm_enable_guest_user_dm_warning": true,
      "realm_enable_guest_user_indicator": true,
      "realm_enable_read_receipts": true,
      "realm_enable_spectator_access": true,
      "realm_filters": [
        "string"
      ],
      "realm_gif_rating_policy": 1,
      "realm_icon_source": "string",
      "realm_icon_url": "https://example.com",
      "realm_incoming_webhook_bots": [
        {}
      ],
      "realm_inline_image_preview": true,
      "realm_inline_url_embed_preview": true,
      "realm_invite_required": true,
      "realm_jitsi_server_url": "https://example.com",
      "realm_linkifiers": [
        "https://example.com"
      ],
      "realm_logo_source": "string",
      "realm_logo_url": "https://example.com",
      "realm_mandatory_topics": true,
      "realm_media_preview_size": 1,
      "realm_message_content_allowed_in_email_notifications": true,
      "realm_message_content_delete_limit_seconds": 1,
      "realm_message_content_edit_limit_seconds": 1,
      "realm_message_edit_history_visibility_policy": "string",
      "realm_message_retention_days": 1,
      "realm_moderation_request_channel_id": 1,
      "realm_move_messages_between_streams_limit_seconds": 1,
      "realm_move_messages_within_stream_limit_seconds": 1,
      "realm_name": "Ava Chen",
      "realm_name_changes_disabled": true,
      "realm_new_stream_announcements_stream_id": 1,
      "realm_night_logo_source": "string",
      "realm_night_logo_url": "https://example.com",
      "realm_non_active_users": [
        "string"
      ],
      "realm_org_type": 1,
      "realm_owner_full_content_access": true,
      "realm_password_auth_enabled": true,
      "realm_plan_type": 1,
      "realm_playgrounds": [
        "string"
      ],
      "realm_presence_disabled": true,
      "realm_push_notifications_enabled": true,
      "realm_push_notifications_enabled_end_timestamp": "string",
      "realm_require_e2ee_push_notifications": true,
      "realm_require_unique_names": true,
      "realm_send_channel_events_messages": true,
      "realm_send_welcome_emails": true,
      "realm_signup_announcements_stream_id": 1,
      "realm_topics_policy": "string",
      "realm_upload_quota_mib": 1,
      "realm_uri": "string",
      "realm_url": "https://example.com",
      "realm_user_groups": [
        {}
      ],
      "realm_user_settings_defaults": {},
      "realm_users": [
        {}
      ],
      "realm_uuid": "string",
      "realm_video_chat_provider": 1,
      "realm_waiting_period_threshold": 1,
      "realm_want_advertise_in_communities_directory": true,
      "realm_welcome_message_custom_text": "string",
      "realm_wildcard_mention_policy": 1,
      "realm_workplace_users_group": 1,
      "realm_zulip_update_announcements_stream_id": 1,
      "recent_private_conversations": [
        "string"
      ],
      "reminders": [
        "string"
      ],
      "result": "string",
      "saved_snippets": [
        "string"
      ],
      "scheduled_messages": [
        "string"
      ],
      "server_avatar_changes_disabled": true,
      "server_can_summarize_topics": true,
      "server_emoji_data_url": "https://example.com",
      "server_generation": 1,
      "server_inline_image_preview": true,
      "server_inline_url_embed_preview": true,
      "server_jitsi_server_url": "https://example.com",
      "server_max_deactivated_realm_deletion_days": 1,
      "server_min_deactivated_realm_deletion_days": 1,
      "server_name_changes_disabled": true,
      "server_needs_upgrade": true,
      "server_presence_offline_threshold_seconds": 1,
      "server_presence_ping_interval_seconds": 1,
      "server_report_message_types": [
        {}
      ],
      "server_supported_permission_settings": {},
      "server_thumbnail_formats": [
        {}
      ],
      "server_timestamp": 1,
      "server_typing_started_expiry_period_milliseconds": 1,
      "server_typing_started_wait_period_milliseconds": 1,
      "server_typing_stopped_wait_period_milliseconds": 1,
      "server_web_public_streams_enabled": true,
      "settings_send_digest_emails": true,
      "starred_messages": [
        "string"
      ],
      "stop_words": [
        "string"
      ],
      "streams": [
        {}
      ],
      "subscriptions": [
        "string"
      ],
      "tenor_api_key": "string",
      "unread_msgs": {},
      "unsubscribed": [
        "string"
      ],
      "upgrade_text_for_wide_organization_logo": "string",
      "user_id": 1,
      "user_settings": {},
      "user_status": {},
      "user_topics": [
        "string"
      ],
      "zulip_feature_level": 1,
      "zulip_merge_base": "string",
      "zulip_plan_is_not_limited": true,
      "zulip_version": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `alert_words` | array |  |
| `avatar_source` | string |  |
| `avatar_url` | string |  |
| `avatar_url_medium` | string |  |
| `can_create_private_streams` | boolean |  |
| `can_create_public_streams` | boolean |  |
| `can_create_streams` | boolean |  |
| `can_create_web_public_streams` | boolean |  |
| `can_invite_others_to_realm` | boolean |  |
| `channel_folders` | array |  |
| `cross_realm_bots` | array<object> |  |
| `custom_profile_field_types` | object |  |
| `custom_profile_fields` | array |  |
| `delivery_email` | string |  |
| `development_environment` | boolean |  |
| `devices` | object |  |
| `drafts` | array |  |
| `email` | string |  |
| `event_queue_longpoll_timeout_seconds` | number |  |
| `full_name` | string |  |
| `gif_rating_policy_options` | object |  |
| `giphy_api_key` | string |  |
| `has_zoom_token` | boolean |  |
| `is_admin` | boolean |  |
| `is_guest` | boolean |  |
| `is_moderator` | boolean |  |
| `is_owner` | boolean |  |
| `jitsi_server_url` | string |  |
| `last_event_id` | number |  |
| `max_avatar_file_size_mib` | number |  |
| `max_bulk_new_subscription_messages` | number |  |
| `max_channel_folder_description_length` | number |  |
| `max_channel_folder_name_length` | number |  |
| `max_file_upload_size_mib` | number |  |
| `max_icon_file_size_mib` | number |  |
| `max_logo_file_size_mib` | number |  |
| `max_message_id` | number |  |
| `max_message_length` | number |  |
| `max_reminder_note_length` | number |  |
| `max_stream_description_length` | number |  |
| `max_stream_name_length` | number |  |
| `max_topic_length` | number |  |
| `msg` | string |  |
| `muted_topics` | array |  |
| `muted_users` | array |  |
| `navigation_tour_video_url` | string |  |
| `navigation_views` | array |  |
| `never_subscribed` | array<object> |  |
| `onboarding_steps` | array<object> |  |
| `password_max_length` | number |  |
| `password_min_guesses` | number |  |
| `password_min_length` | number |  |
| `presence_last_update_id` | number |  |
| `presences` | object |  |
| `queue_id` | string |  |
| `realm_allow_edit_history` | boolean |  |
| `realm_allow_message_editing` | boolean |  |
| `realm_authentication_methods` | object |  |
| `realm_available_video_chat_providers` | object |  |
| `realm_avatar_changes_disabled` | boolean |  |
| `realm_billing` | object |  |
| `realm_bot_domain` | string |  |
| `realm_bots` | array |  |
| `realm_can_access_all_users_group` | number |  |
| `realm_can_add_custom_emoji_group` | number |  |
| `realm_can_add_subscribers_group` | number |  |
| `realm_can_create_bots_group` | number |  |
| `realm_can_create_groups` | number |  |
| `realm_can_create_private_channel_group` | number |  |
| `realm_can_create_public_channel_group` | number |  |
| `realm_can_create_web_public_channel_group` | number |  |
| `realm_can_create_write_only_bots_group` | number |  |
| `realm_can_delete_any_message_group` | number |  |
| `realm_can_delete_own_message_group` | number |  |
| `realm_can_invite_users_group` | number |  |
| `realm_can_manage_all_groups` | number |  |
| `realm_can_manage_billing_group` | number |  |
| `realm_can_mention_many_users_group` | number |  |
| `realm_can_move_messages_between_channels_group` | number |  |
| `realm_can_move_messages_between_topics_group` | number |  |
| `realm_can_resolve_topics_group` | number |  |
| `realm_can_set_delete_message_policy_group` | number |  |
| `realm_can_set_topics_policy_group` | number |  |
| `realm_can_summarize_topics_group` | number |  |
| `realm_create_multiuse_invite_group` | number |  |
| `realm_create_private_stream_policy` | number |  |
| `realm_create_public_stream_policy` | number |  |
| `realm_create_web_public_stream_policy` | number |  |
| `realm_date_created` | number |  |
| `realm_default_avatar_source` | string |  |
| `realm_default_code_block_language` | string |  |
| `realm_default_external_accounts` | object |  |
| `realm_default_language` | string |  |
| `realm_default_stream_groups` | array |  |
| `realm_default_streams` | array<number> |  |
| `realm_description` | string |  |
| `realm_digest_emails_enabled` | boolean |  |
| `realm_digest_weekday` | number |  |
| `realm_direct_message_initiator_group` | number |  |
| `realm_direct_message_permission_group` | number |  |
| `realm_disallow_disposable_email_addresses` | boolean |  |
| `realm_domains` | array |  |
| `realm_email_auth_enabled` | boolean |  |
| `realm_email_changes_disabled` | boolean |  |
| `realm_emails_restricted_to_domains` | boolean |  |
| `realm_embedded_bots` | array<object> |  |
| `realm_emoji` | object |  |
| `realm_empty_topic_display_name` | string |  |
| `realm_enable_guest_user_dm_warning` | boolean |  |
| `realm_enable_guest_user_indicator` | boolean |  |
| `realm_enable_read_receipts` | boolean |  |
| `realm_enable_spectator_access` | boolean |  |
| `realm_filters` | array |  |
| `realm_gif_rating_policy` | number |  |
| `realm_icon_source` | string |  |
| `realm_icon_url` | string |  |
| `realm_incoming_webhook_bots` | array<object> |  |
| `realm_inline_image_preview` | boolean |  |
| `realm_inline_url_embed_preview` | boolean |  |
| `realm_invite_required` | boolean |  |
| `realm_jitsi_server_url` | string |  |
| `realm_linkifiers` | array |  |
| `realm_logo_source` | string |  |
| `realm_logo_url` | string |  |
| `realm_mandatory_topics` | boolean |  |
| `realm_media_preview_size` | number |  |
| `realm_message_content_allowed_in_email_notifications` | boolean |  |
| `realm_message_content_delete_limit_seconds` | number |  |
| `realm_message_content_edit_limit_seconds` | number |  |
| `realm_message_edit_history_visibility_policy` | string |  |
| `realm_message_retention_days` | number |  |
| `realm_moderation_request_channel_id` | number |  |
| `realm_move_messages_between_streams_limit_seconds` | number |  |
| `realm_move_messages_within_stream_limit_seconds` | number |  |
| `realm_name` | string |  |
| `realm_name_changes_disabled` | boolean |  |
| `realm_new_stream_announcements_stream_id` | number |  |
| `realm_night_logo_source` | string |  |
| `realm_night_logo_url` | string |  |
| `realm_non_active_users` | array |  |
| `realm_org_type` | number |  |
| `realm_owner_full_content_access` | boolean |  |
| `realm_password_auth_enabled` | boolean |  |
| `realm_plan_type` | number |  |
| `realm_playgrounds` | array |  |
| `realm_presence_disabled` | boolean |  |
| `realm_push_notifications_enabled` | boolean |  |
| `realm_push_notifications_enabled_end_timestamp` | string |  |
| `realm_require_e2ee_push_notifications` | boolean |  |
| `realm_require_unique_names` | boolean |  |
| `realm_send_channel_events_messages` | boolean |  |
| `realm_send_welcome_emails` | boolean |  |
| `realm_signup_announcements_stream_id` | number |  |
| `realm_topics_policy` | string |  |
| `realm_upload_quota_mib` | number |  |
| `realm_uri` | string |  |
| `realm_url` | string |  |
| `realm_user_groups` | array<object> |  |
| `realm_user_settings_defaults` | object |  |
| `realm_users` | array<object> |  |
| `realm_uuid` | string |  |
| `realm_video_chat_provider` | number |  |
| `realm_waiting_period_threshold` | number |  |
| `realm_want_advertise_in_communities_directory` | boolean |  |
| `realm_welcome_message_custom_text` | string |  |
| `realm_wildcard_mention_policy` | number |  |
| `realm_workplace_users_group` | number |  |
| `realm_zulip_update_announcements_stream_id` | number |  |
| `recent_private_conversations` | array |  |
| `reminders` | array |  |
| `result` | string |  |
| `saved_snippets` | array |  |
| `scheduled_messages` | array |  |
| `server_avatar_changes_disabled` | boolean |  |
| `server_can_summarize_topics` | boolean |  |
| `server_emoji_data_url` | string |  |
| `server_generation` | number |  |
| `server_inline_image_preview` | boolean |  |
| `server_inline_url_embed_preview` | boolean |  |
| `server_jitsi_server_url` | string |  |
| `server_max_deactivated_realm_deletion_days` | number |  |
| `server_min_deactivated_realm_deletion_days` | number |  |
| `server_name_changes_disabled` | boolean |  |
| `server_needs_upgrade` | boolean |  |
| `server_presence_offline_threshold_seconds` | number |  |
| `server_presence_ping_interval_seconds` | number |  |
| `server_report_message_types` | array<object> |  |
| `server_supported_permission_settings` | object |  |
| `server_thumbnail_formats` | array<object> |  |
| `server_timestamp` | number |  |
| `server_typing_started_expiry_period_milliseconds` | number |  |
| `server_typing_started_wait_period_milliseconds` | number |  |
| `server_typing_stopped_wait_period_milliseconds` | number |  |
| `server_web_public_streams_enabled` | boolean |  |
| `settings_send_digest_emails` | boolean |  |
| `starred_messages` | array |  |
| `stop_words` | array<string> |  |
| `streams` | array<object> |  |
| `subscriptions` | array |  |
| `tenor_api_key` | string |  |
| `unread_msgs` | object |  |
| `unsubscribed` | array |  |
| `upgrade_text_for_wide_organization_logo` | string |  |
| `user_id` | number |  |
| `user_settings` | object |  |
| `user_status` | object |  |
| `user_topics` | array |  |
| `zulip_feature_level` | number |  |
| `zulip_merge_base` | string |  |
| `zulip_plan_is_not_limited` | boolean |  |
| `zulip_version` | string |  |

## Native endpoint

Through the native Zulip API, this operation is `POST /register` (base URL `{{credentials.site}}/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/register-event-queue.md) for the provider-specific parameters and requirements.


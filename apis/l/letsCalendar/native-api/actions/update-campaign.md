# Update Campaign with Let's Calendar

Updates an existing campaign in Let's Calendar.

## Endpoint

- **Method:** `PUT`
- **Path:** `campaign/:campaignId`
- **Base URL:** `https://panel.letscalendar.com/api/lc`
- **Official documentation:** [Update Campaign](https://panel.letscalendar.com/docs#apis-PUTapi-lc-campaign--campaign_id-)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaign_id` | path | `string` | yes | The unique identifier of the campaign to update. |
| `title` | body | `string` | yes | The title of the campaign. |
| `subject` | body | `string` | yes | The email subject line. |
| `event_type` | body | `string` | yes | Type of event: online, offline, or physical. |
| `sender_email_id` | body | `number` | yes | ID of the sender email to use. |
| `start_date` | body | `string` | yes | Start date in Y-m-d format. |
| `start_time` | body | `string` | yes | Start time in H:i format. |
| `end_date` | body | `string` | yes | End date in Y-m-d format. |
| `end_time` | body | `string` | yes | End time in H:i format. |
| `timezone` | body | `string` | yes | Timezone for the event. |
| `description` | body | `string` | yes | Description of the campaign. |
| `email_content` | body | `string` | yes | HTML content for the invite email body. |
| `location` | body | `string` | no | Physical location for the event when the event type is physical. |
| `login_url` | body | `string` | no | Common login URL for offline events. |

# Process Plan: Convert Users IDs to Objects



```
GET https://connect.mindcloud.co/v1/universal/processPlan/latest/actions/convert-users-i-ds-to-objects
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Process Plan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/processPlan/latest/actions/convert-users-i-ds-to-objects?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/processPlan/latest/actions/convert-users-i-ds-to-objects?${params}`, {
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
      "user_list": [
        {
          "usr_24_hour_time": true,
          "usr_acc_id": "string",
          "usr_assignment_emails": true,
          "usr_created_date_local": "2026-05-07T12:00:00.000Z",
          "usr_created_usr_id": "string",
          "usr_date_format": 1,
          "usr_email_address": "ava@example.com",
          "usr_first_name": "Ava",
          "usr_full_name": "Ava Chen",
          "usr_fullscreen_tasks": true,
          "usr_id": "string",
          "usr_language": "string",
          "usr_last_activity_date_local": "2026-05-07T12:00:00.000Z",
          "usr_last_name": "Chen",
          "usr_message_emails": true,
          "usr_modified_date_local": "2026-05-07T12:00:00.000Z",
          "usr_modified_usr_id": "string",
          "usr_profile_pic_url": "https://example.com",
          "usr_require_mfa": true,
          "usr_ug_name_list": [
            "Ava Chen"
          ],
          "usr_utc_offset": 1
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
| `user_list[].usr_24_hour_time` | boolean |  |
| `user_list[].usr_acc_id` | string |  |
| `user_list[].usr_assignment_emails` | boolean |  |
| `user_list[].usr_created_date_local` | date |  |
| `user_list[].usr_created_usr_id` | string |  |
| `user_list[].usr_date_format` | number |  |
| `user_list[].usr_email_address` | string |  |
| `user_list[].usr_first_name` | string |  |
| `user_list[].usr_full_name` | string |  |
| `user_list[].usr_fullscreen_tasks` | boolean |  |
| `user_list[].usr_id` | string |  |
| `user_list[].usr_language` | string |  |
| `user_list[].usr_last_activity_date_local` | date |  |
| `user_list[].usr_last_name` | string |  |
| `user_list[].usr_message_emails` | boolean |  |
| `user_list[].usr_modified_date_local` | date |  |
| `user_list[].usr_modified_usr_id` | string |  |
| `user_list[].usr_profile_pic_url` | string |  |
| `user_list[].usr_require_mfa` | boolean |  |
| `user_list[].usr_ug_name_list[]` | string |  |
| `user_list[].usr_utc_offset` | number |  |

## Native endpoint

Through the native Process Plan API, this operation is `POST /user/id_list/to_object/list` (base URL `https://apius0.processplan.com/api/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/convert-users-i-ds-to-objects.md) for the provider-specific parameters and requirements.


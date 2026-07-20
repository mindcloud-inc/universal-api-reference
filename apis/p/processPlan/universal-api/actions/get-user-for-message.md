# Process Plan: Get User for Message



```
GET https://connect.mindcloud.co/v1/universal/processPlan/latest/actions/get-user-for-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Process Plan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/processPlan/latest/actions/get-user-for-message?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/processPlan/latest/actions/get-user-for-message?${params}`, {
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
| `messageId` | string | no | Message ID. |
| `userId` | string | no | User ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "msg_acc_id": "string",
      "msg_created_date_local": "2026-05-07T12:00:00.000Z",
      "msg_created_usr_id": "string",
      "msg_has_fl": true,
      "msg_id": "string",
      "msg_ih_id": "string",
      "msg_ih_obj": {
        "ih_created_date_local": "2026-05-07T12:00:00.000Z",
        "ih_id": "string",
        "ih_instance_description": "string",
        "ih_personal_task": true,
        "ih_progress_percentage": 1,
        "ih_test_mode": true,
        "ih_th_id": "string",
        "ih_th_obj": {
          "th_icon_name": "Ava Chen",
          "th_id": "string",
          "th_name": "Ava Chen"
        }
      },
      "msg_modified_date_local": "2026-05-07T12:00:00.000Z",
      "msg_modified_usr_id": "string",
      "msg_modified_usr_obj": {
        "usr_email_address": "ava@example.com",
        "usr_first_name": "Ava",
        "usr_full_name": "Ava Chen",
        "usr_id": "string",
        "usr_last_name": "Chen",
        "usr_profile_pic_url": "https://example.com"
      },
      "msg_text": "string",
      "msg_th_id": "string",
      "msg_th_obj": {
        "th_icon_name": "Ava Chen",
        "th_id": "string",
        "th_name": "Ava Chen"
      },
      "msg_thread_name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `msg_acc_id` | string |  |
| `msg_created_date_local` | date |  |
| `msg_created_usr_id` | string |  |
| `msg_has_fl` | boolean |  |
| `msg_id` | string |  |
| `msg_ih_id` | string |  |
| `msg_ih_obj.ih_created_date_local` | date |  |
| `msg_ih_obj.ih_id` | string |  |
| `msg_ih_obj.ih_instance_description` | string |  |
| `msg_ih_obj.ih_personal_task` | boolean |  |
| `msg_ih_obj.ih_progress_percentage` | number |  |
| `msg_ih_obj.ih_test_mode` | boolean |  |
| `msg_ih_obj.ih_th_id` | string |  |
| `msg_ih_obj.ih_th_obj.th_icon_name` | string |  |
| `msg_ih_obj.ih_th_obj.th_id` | string |  |
| `msg_ih_obj.ih_th_obj.th_name` | string |  |
| `msg_modified_date_local` | date |  |
| `msg_modified_usr_id` | string |  |
| `msg_modified_usr_obj.usr_email_address` | string |  |
| `msg_modified_usr_obj.usr_first_name` | string |  |
| `msg_modified_usr_obj.usr_full_name` | string |  |
| `msg_modified_usr_obj.usr_id` | string |  |
| `msg_modified_usr_obj.usr_last_name` | string |  |
| `msg_modified_usr_obj.usr_profile_pic_url` | string |  |
| `msg_text` | string |  |
| `msg_th_id` | string |  |
| `msg_th_obj.th_icon_name` | string |  |
| `msg_th_obj.th_id` | string |  |
| `msg_th_obj.th_name` | string |  |
| `msg_thread_name` | string |  |

## Native endpoint

Through the native Process Plan API, this operation is `GET /message/:messageId/user/:userId` (base URL `https://apius0.processplan.com/api/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user-for-message.md) for the provider-specific parameters and requirements.


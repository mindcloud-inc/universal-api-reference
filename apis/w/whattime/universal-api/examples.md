# Whattime Universal API Examples

These examples use the MindCloud API key and Whattime connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get My User



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/whattime/latest/actions/get-my-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/whattime/latest/actions/get-my-user?${params}`, {
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
      "code": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "name": "Ava Chen",
      "organization": {
        "code": "string",
        "created_at": "2026-05-07T12:00:00.000Z",
        "name": "Ava Chen",
        "updated_at": "2026-05-07T12:00:00.000Z",
        "uri": "string"
      },
      "role": "string",
      "slug": "string",
      "time_zone": "string",
      "updated_at": "2026-05-07T12:00:00.000Z",
      "uri": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get My User action reference](actions/get-my-user.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/whattime/latest/actions/get-my-user).

## Cancel Schedule



```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/whattime/latest/actions/cancel-schedule" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "code": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/whattime/latest/actions/cancel-schedule', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "code": "string"
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
      "calendar": {
        "active": true,
        "alarm": {
          "email_guest": true,
          "email_guest_cancel_title": "ava@example.com",
          "email_guest_content": "ava@example.com",
          "email_guest_title": "ava@example.com"
        },
        "code": "string",
        "color": "string",
        "description": "string",
        "description_raw": "string",
        "kind": "string",
        "locations": {
          "address": "string",
          "address_link": "https://example.com",
          "answer": "string",
          "direct": "string",
          "kind": "string",
          "member_email": "ava@example.com",
          "phone": "string",
          "remote_password": "string",
          "remote_url": "https://example.com"
        },
        "max_invitee": 1,
        "members": {
          "created_at": "2026-05-07T12:00:00.000Z",
          "organizer": true,
          "updated_at": "2026-05-07T12:00:00.000Z",
          "user": {}
        },
        "name": "Ava Chen",
        "order": 1,
        "reservation_url": "https://example.com",
        "secret": true,
        "show_remain": true,
        "slug": "string",
        "survey": {
          "email_etc_required": true,
          "email_required": true,
          "phone_required": true,
          "questions": [
            {}
          ]
        },
        "team": {
          "created_at": "2026-05-07T12:00:00.000Z",
          "img_url": "https://example.com",
          "logo_url": "https://example.com",
          "message": "string",
          "name": "Ava Chen",
          "share_img_url": "https://example.com",
          "slug": "string",
          "updated_at": "2026-05-07T12:00:00.000Z"
        },
        "time": {
          "after_buffer": 1,
          "after_calendar_buffer": 1,
          "availability_kind": "string",
          "availability_time": {},
          "before_buffer": 1,
          "before_calendar_buffer": 1,
          "duration": 1,
          "duration_kind": "string",
          "guest_min_time": 1,
          "guest_min_time_kind": "string",
          "incre": 1,
          "prepare": 1,
          "prepare_kind": "string",
          "range_after_day": 1,
          "range_after_day_kind": "string",
          "range_end": "2026-05-07T12:00:00.000Z",
          "range_kind": "string",
          "range_start": "2026-05-07T12:00:00.000Z"
        },
        "uri": "string"
      },
      "code": "string",
      "reservation_code": "string",
      "team": {
        "created_at": "2026-05-07T12:00:00.000Z",
        "img_url": "https://example.com",
        "logo_url": "https://example.com",
        "message": "string",
        "name": "Ava Chen",
        "share_img_url": "https://example.com",
        "slug": "string",
        "updated_at": "2026-05-07T12:00:00.000Z"
      },
      "uri": "string"
    }
  ],
  "meta": {}
}
```

See the full [Cancel Schedule action reference](actions/cancel-schedule.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/whattime/latest/actions/cancel-schedule).

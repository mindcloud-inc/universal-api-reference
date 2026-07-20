# Whattime: Upsert Calendar



```
PUT https://connect.mindcloud.co/v1/universal/whattime/latest/actions/upsert-calendar
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Whattime `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/whattime/latest/actions/upsert-calendar" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/whattime/latest/actions/upsert-calendar', {
  method: 'PUT',
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

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `code` | string | no | 예약 페이지 코드 |
| `url` | string | no | 예약 페이지 주소 |
| `kind` | string | no | 종류 * `one_to_one` - 1:1 * `groups` - 그룹 * `collective` - 여러명이 주최 * `round_robin` - 여러명 돌아가며 주최 |
| `name` | string | no |  |
| `slug` | string | no | 단축 이름 |
| `color` | string | no | 구별 색깔 |
| `description` | string | no | 예약 페이지 설명 (HTML) |
| `maxInvitee` | number | no | 최대 정원수 (그룹 예약) |
| `showRemain` | boolean | no | 잔여 횟수 노출 (그룹 예약) |
| `order` | number | no | 우선순위 |
| `secret` | boolean | no | 일정 예약 숨기기 |
| `active` | boolean | no | 활성화 여부 |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
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
        "user": {
          "code": "string",
          "created_at": "2026-05-07T12:00:00.000Z",
          "email": "ava@example.com",
          "name": "Ava Chen",
          "organization": {},
          "role": "string",
          "slug": "string",
          "time_zone": "string",
          "updated_at": "2026-05-07T12:00:00.000Z",
          "uri": "string"
        }
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
        "questions": {
          "items": [
            "string"
          ],
          "kind": "string",
          "on": true,
          "required": true,
          "title": "string"
        }
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
        "availability_time": {
          "overrides": [
            {}
          ],
          "time_zone": "string",
          "wday_rules": [
            {}
          ]
        },
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
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `code` | string |  |
| `color` | string |  |
| `description` | string |  |
| `description_raw` | string |  |
| `kind` | string |  |
| `locations` | array<object> |  |
| `locations.address` | string |  |
| `locations.address_link` | string |  |
| `locations.answer` | string |  |
| `locations.direct` | string |  |
| `locations.kind` | string |  |
| `locations.member_email` | string |  |
| `locations.phone` | string |  |
| `locations.remote_password` | string |  |
| `locations.remote_url` | string |  |
| `max_invitee` | number |  |
| `members` | array<object> |  |
| `members.created_at` | date |  |
| `members.organizer` | boolean |  |
| `members.updated_at` | date |  |
| `members.user` | object |  |
| `members.user.code` | string |  |
| `members.user.created_at` | date |  |
| `members.user.email` | string |  |
| `members.user.name` | string |  |
| `members.user.organization` | object |  |
| `members.user.role` | string |  |
| `members.user.slug` | string |  |
| `members.user.time_zone` | string |  |
| `members.user.updated_at` | date |  |
| `members.user.uri` | string |  |
| `name` | string |  |
| `order` | number |  |
| `reservation_url` | string |  |
| `secret` | boolean |  |
| `show_remain` | boolean |  |
| `slug` | string |  |
| `survey` | object |  |
| `survey.email_etc_required` | boolean |  |
| `survey.email_required` | boolean |  |
| `survey.phone_required` | boolean |  |
| `survey.questions` | array<object> |  |
| `survey.questions.items` | array<string> |  |
| `survey.questions.kind` | string |  |
| `survey.questions.on` | boolean |  |
| `survey.questions.required` | boolean |  |
| `survey.questions.title` | string |  |
| `team` | object |  |
| `team.created_at` | date |  |
| `team.img_url` | string |  |
| `team.logo_url` | string |  |
| `team.message` | string |  |
| `team.name` | string |  |
| `team.share_img_url` | string |  |
| `team.slug` | string |  |
| `team.updated_at` | date |  |
| `time` | object |  |
| `time.after_buffer` | number |  |
| `time.after_calendar_buffer` | number |  |
| `time.availability_kind` | string |  |
| `time.availability_time` | object |  |
| `time.availability_time.overrides` | array<object> |  |
| `time.availability_time.time_zone` | string |  |
| `time.availability_time.wday_rules` | array<object> |  |
| `time.before_buffer` | number |  |
| `time.before_calendar_buffer` | number |  |
| `time.duration` | number |  |
| `time.duration_kind` | string |  |
| `time.guest_min_time` | number |  |
| `time.guest_min_time_kind` | string |  |
| `time.incre` | number |  |
| `time.prepare` | number |  |
| `time.prepare_kind` | string |  |
| `time.range_after_day` | number |  |
| `time.range_after_day_kind` | string |  |
| `time.range_end` | date |  |
| `time.range_kind` | string |  |
| `time.range_start` | date |  |
| `uri` | string |  |

## Native endpoint

Through the native Whattime API, this operation is `POST /calendars/upsert` (base URL `https://api.whattime.co.kr/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upsert-calendar.md) for the provider-specific parameters and requirements.


# Whattime: List Reservations



```
GET https://connect.mindcloud.co/v1/universal/whattime/latest/actions/list-reservations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Whattime `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/whattime/latest/actions/list-reservations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/whattime/latest/actions/list-reservations?${params}`, {
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
| `organization` | string | no | Organization uri (User 모델에 organization.uri 를 참고해 주세요) |
| `user` | string | no | User uri (User 모델에 uri 를 확인해 주세요) |
| `status` | string | no | 상태 |
| `email` | string | no | 이메일 |
| `name` | string | no | 이름 |
| `minStartAt` | string | no | 시간 검색 시작시간 |
| `maxStartAt` | string | no | 시간 검색 종료시간 |
| `sort` | string | no | 정렬 필드 `id` : 생성일, `start_at` : 시작시간 |
| `order` | string | no | 오름,내림 차순 |
| `per` | number | no | 가져올 개수 |
| `pageToken` | string | no | 가져올 다음페이지 토큰 |

## Response

```json
{
  "success": true,
  "data": [
    {
      "calendar": {
        "active": true,
        "alarm": {
          "email_guest": true,
          "email_guest_cancel_content": "ava@example.com",
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

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `calendar` | object |  |
| `calendar.active` | boolean |  |
| `calendar.alarm` | object |  |
| `calendar.alarm.email_guest` | boolean |  |
| `calendar.alarm.email_guest_cancel_content` | string |  |
| `calendar.alarm.email_guest_cancel_title` | string |  |
| `calendar.alarm.email_guest_content` | string |  |
| `calendar.alarm.email_guest_title` | string |  |
| `calendar.code` | string |  |
| `calendar.color` | string |  |
| `calendar.description` | string |  |
| `calendar.description_raw` | string |  |
| `calendar.kind` | string |  |
| `calendar.locations` | array<object> |  |
| `calendar.locations.address` | string |  |
| `calendar.locations.address_link` | string |  |
| `calendar.locations.answer` | string |  |
| `calendar.locations.direct` | string |  |
| `calendar.locations.kind` | string |  |
| `calendar.locations.member_email` | string |  |
| `calendar.locations.phone` | string |  |
| `calendar.locations.remote_password` | string |  |
| `calendar.locations.remote_url` | string |  |
| `calendar.max_invitee` | number |  |
| `calendar.members` | array<object> |  |
| `calendar.members.created_at` | date |  |
| `calendar.members.organizer` | boolean |  |
| `calendar.members.updated_at` | date |  |
| `calendar.members.user` | object |  |
| `calendar.name` | string |  |
| `calendar.order` | number |  |
| `calendar.reservation_url` | string |  |
| `calendar.secret` | boolean |  |
| `calendar.show_remain` | boolean |  |
| `calendar.slug` | string |  |
| `calendar.survey` | object |  |
| `calendar.survey.email_etc_required` | boolean |  |
| `calendar.survey.email_required` | boolean |  |
| `calendar.survey.phone_required` | boolean |  |
| `calendar.survey.questions` | array<object> |  |
| `calendar.team` | object |  |
| `calendar.team.created_at` | date |  |
| `calendar.team.img_url` | string |  |
| `calendar.team.logo_url` | string |  |
| `calendar.team.message` | string |  |
| `calendar.team.name` | string |  |
| `calendar.team.share_img_url` | string |  |
| `calendar.team.slug` | string |  |
| `calendar.team.updated_at` | date |  |
| `calendar.time` | object |  |
| `calendar.time.after_buffer` | number |  |
| `calendar.time.after_calendar_buffer` | number |  |
| `calendar.time.availability_kind` | string |  |
| `calendar.time.availability_time` | object |  |
| `calendar.time.before_buffer` | number |  |
| `calendar.time.before_calendar_buffer` | number |  |
| `calendar.time.duration` | number |  |
| `calendar.time.duration_kind` | string |  |
| `calendar.time.guest_min_time` | number |  |
| `calendar.time.guest_min_time_kind` | string |  |
| `calendar.time.incre` | number |  |
| `calendar.time.prepare` | number |  |
| `calendar.time.prepare_kind` | string |  |
| `calendar.time.range_after_day` | number |  |
| `calendar.time.range_after_day_kind` | string |  |
| `calendar.time.range_end` | date |  |
| `calendar.time.range_kind` | string |  |
| `calendar.time.range_start` | date |  |
| `calendar.uri` | string |  |
| `code` | string |  |
| `team` | object |  |
| `team.created_at` | date |  |
| `team.img_url` | string |  |
| `team.logo_url` | string |  |
| `team.message` | string |  |
| `team.name` | string |  |
| `team.share_img_url` | string |  |
| `team.slug` | string |  |
| `team.updated_at` | date |  |
| `uri` | string |  |

## Native endpoint

Through the native Whattime API, this operation is `GET /reservations` (base URL `https://api.whattime.co.kr/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-reservations.md) for the provider-specific parameters and requirements.


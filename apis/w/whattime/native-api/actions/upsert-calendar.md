# Upsert Calendar with Whattime

## Endpoint

- **Method:** `POST`
- **Path:** `/calendars/upsert`
- **Base URL:** `https://api.whattime.co.kr/v1`
- **Official documentation:** [Upsert Calendar](https://developer.whattime.co.kr/swagger#/Calendar/calendarsUpsert)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `code` | body | `string` | no | 예약 페이지 코드 |
| `url` | body | `string` | no | 예약 페이지 주소 |
| `kind` | body | `string` | no | 종류   * `one_to_one` - 1:1   * `groups` - 그룹   * `collective` - 여러명이 주최   * `round_robin` - 여러명 돌아가며 주최 |
| `name` | body | `string` | no | — |
| `slug` | body | `string` | no | 단축 이름 |
| `color` | body | `string` | no | 구별 색깔 |
| `description` | body | `string` | no | 예약 페이지 설명 (HTML) |
| `max_invitee` | body | `number` | no | 최대 정원수 (그룹 예약) |
| `show_remain` | body | `boolean` | no | 잔여 횟수 노출 (그룹 예약) |
| `order` | body | `number` | no | 우선순위 |
| `secret` | body | `boolean` | no | 일정 예약 숨기기 |
| `active` | body | `boolean` | no | 활성화 여부 |

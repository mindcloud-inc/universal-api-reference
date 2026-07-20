# Update Basic Availability with Whattime

## Endpoint

- **Method:** `PUT`
- **Path:** `/availabilities/basic`
- **Base URL:** `https://api.whattime.co.kr/v1`
- **Official documentation:** [Update Basic Availability](https://developer.whattime.co.kr/swagger#/Availability/availabilitiesBasicUpdateByCode)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `user` | query | `string` | no | User uri (User 모델에 uri 를 확인해 주세요) |
| `name` | body | `string` | yes | 이름 |
| `time_zone` | body | `string` | no | 타임존 |
| `default` | body | `boolean` | no | 기본 여부 |
| `rules[]` | body | `array<object>` | no | 요일별 가능한 시간 |
| `overrides[]` | body | `array<object>` | no | 가능한 시간 예외 날짜 |

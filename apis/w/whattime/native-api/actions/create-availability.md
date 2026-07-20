# Create Availability with Whattime

## Endpoint

- **Method:** `POST`
- **Path:** `/availabilities`
- **Base URL:** `https://api.whattime.co.kr/v1`
- **Official documentation:** [Create Availability](https://developer.whattime.co.kr/swagger#/Availability/availabilitiesCreate)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `user` | body | `string` | no | User uri |
| `name` | body | `string` | yes | 이름 |
| `time_zone` | body | `string` | no | 타임존 |
| `default` | body | `boolean` | no | 기본 여부 |
| `rules[]` | body | `array<object>` | no | 요일별 가능한 시간 |
| `overrides[]` | body | `array<object>` | no | 가능한 시간 예외 날짜 |

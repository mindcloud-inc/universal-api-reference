# Reschedule Schedule with Whattime

## Endpoint

- **Method:** `POST`
- **Path:** `/schedules/:code/reschedule`
- **Base URL:** `https://api.whattime.co.kr/v1`
- **Official documentation:** [Reschedule Schedule](https://developer.whattime.co.kr/swagger#/Schedule/schedulesReschedule)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `code` | path | `string` | yes | Resource Code |
| `date` | body | `date` | yes | 변경 날짜 |
| `time` | body | `string` | yes | 변경 시간 |
| `time_zone` | body | `string` | no | 타임존 |
| `reschedule_reason` | body | `string` | no | 변경 사유 |

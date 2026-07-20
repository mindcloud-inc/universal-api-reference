# Create Schedule with Whattime

## Endpoint

- **Method:** `POST`
- **Path:** `/schedules`
- **Base URL:** `https://api.whattime.co.kr/v1`
- **Official documentation:** [Create Schedule](https://developer.whattime.co.kr/swagger#/Schedule/schedulesCreate)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `calendar` | body | `string` | no | Calendar uri |
| `date` | body | `date` | yes | 변경 날짜 |
| `time` | body | `string` | yes | 변경 시간 |
| `time_zone` | body | `string` | no | 타임존 |
| `name` | body | `string` | yes | 이름 |
| `email` | body | `string` | no | 이메일 |
| `phone` | body | `string` | no | 전화번호, 국가번호 포함되어도 무관 |
| `questions[]` | body | `array<object>` | no | 설문 답변 |

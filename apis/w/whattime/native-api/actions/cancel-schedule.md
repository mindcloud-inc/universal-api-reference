# Cancel Schedule with Whattime

## Endpoint

- **Method:** `POST`
- **Path:** `/schedules/:code/cancel`
- **Base URL:** `https://api.whattime.co.kr/v1`
- **Official documentation:** [Cancel Schedule](https://developer.whattime.co.kr/swagger#/Schedule/schedulesCancel)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `code` | path | `string` | yes | Resource Code |
| `cancel_reason` | body | `string` | no | 취소 사유 |
| `cancel_guest_alarm` | body | `boolean` | no | 게스트에게 알림을 보낼지 여부 |

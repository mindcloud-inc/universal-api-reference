# Create Webhook with Whattime

## Endpoint

- **Method:** `POST`
- **Path:** `/webhooks`
- **Base URL:** `https://api.whattime.co.kr/v1`
- **Official documentation:** [Create Webhook](https://developer.whattime.co.kr/swagger#/Webhook/webhooksCreate)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `kind` | body | `string` | yes | 콜백 종류   * `schedule_created` - 예약 생성   * `schedule_canceled` - 예약 취소   * `user_changed` - 유저 정보 변경   * `user_withdraw` - 유저 탈퇴 |
| `organization` | body | `string` | no | Organization uri |
| `user` | body | `string` | no | User uri |
| `callback_url` | body | `string` | yes | 콜백 받을 주소 |
| `scope` | body | `string` | no | 콜백 종류   * `user` - 특정 유저   * `organization` - 조직 전체 |
| `signing_key` | body | `string` | no | 보안을 위한 사이닝 키 <br> `WhatTime-Webhook-Signature` : `t={timestamp},v1={signing_key}` 가 헤더값에 추가됩니다. |

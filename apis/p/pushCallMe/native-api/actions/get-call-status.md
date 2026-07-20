# Get Call Status with PushCallMe

Retrieves call status details from PushCallMe.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/calls/:requestId`
- **Base URL:** `https://pushcall.me`
- **Official documentation:** [Get Call Status](https://pushcall.me/docs/phone-call-via-http-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `requestId` | path | `string` | yes | Request identifier returned by the Make Phone Call action. |

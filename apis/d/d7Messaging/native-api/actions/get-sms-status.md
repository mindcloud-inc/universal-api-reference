# Get SMS Status with D7 Messaging

Retrieves SMS delivery status from D7 Messaging.

## Endpoint

- **Method:** `GET`
- **Path:** `/report/v1/message-log/:request_id`
- **Base URL:** `https://api.d7networks.com`
- **Official documentation:** [Get SMS Status](https://d7networks.com/docs/sms/get-status/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `request_id` | path | `string` | yes | Request ID returned by Send SMS. |

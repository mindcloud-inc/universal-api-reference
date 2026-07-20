# Get SMS Message Status with D7 Networks

Retrieves SMS delivery status from D7 Networks.

## Endpoint

- **Method:** `GET`
- **Path:** `/report/v1/message-log/:requestId`
- **Base URL:** `https://api.d7networks.com`
- **Official documentation:** [Get SMS Message Status](https://d7networks.com/docs/sms/get-status/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `request_id` | path | `string` | yes | Request ID returned by the Send SMS action. |

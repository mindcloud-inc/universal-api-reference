# Get Viber Status with D7 Messaging

Retrieves Viber delivery status from D7 Messaging.

## Endpoint

- **Method:** `GET`
- **Path:** `/report/v1/viber-log/:request_id`
- **Base URL:** `https://api.d7networks.com`
- **Official documentation:** [Get Viber Status](https://d7networks.com/docs/viber/get-status/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `request_id` | path | `string` | yes | Request ID returned by Send Viber Message. |

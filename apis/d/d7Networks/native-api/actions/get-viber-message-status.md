# Get Viber Message Status with D7 Networks

Retrieves Viber message status from D7 Networks.

## Endpoint

- **Method:** `GET`
- **Path:** `/report/v1/viber-log/:requestId`
- **Base URL:** `https://api.d7networks.com`
- **Official documentation:** [Get Viber Message Status](https://d7networks.com/docs/viber/get-status/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `request_id` | path | `string` | yes | Request ID returned by the Send Viber Message action. |

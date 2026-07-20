# List Customer Schedules with Pinghome

Retrieves customer schedules from Pinghome.

## Endpoint

- **Method:** `GET`
- **Path:** `/incident-query/v1/customer/:id/schedule`
- **Base URL:** `https://api.pinghome.io`
- **Official documentation:** [List Customer Schedules](https://docs.pinghome.io/incident-management/incident-schedule-management/get-customer-schedules/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | no | The unique ID of the customer whose schedules are being retrieved. |

# List Events with ECAL

Retrieves events from ECAL.

## Endpoint

- **Method:** `GET`
- **Path:** `/event/`
- **Base URL:** `https://api.ecal.com/apiv2`
- **Official documentation:** [List Events](https://docs.ecal.com/reference/apiv2/event.html#get-apiv2event)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `startDate` | query | `date` | no | Filter events from this date. |
| `endDate` | query | `date` | no | Filter events through this date. |
| `timezone` | query | `string` | no | Timezone used when filtering date/time values. |
| `showPastEvents` | query | `boolean` | no | Whether to include past events in the response. |
